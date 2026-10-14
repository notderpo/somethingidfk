---
name: agner-cloud-conventions
description: Conventions for the agner.cloud self-hosted platform - folder layout, Docker Compose style, Cloudflare Tunnel routing, Pocket ID OIDC, NetBird-only services, naming. Use for any infra or deployment work.
---

# agner.cloud conventions

## Platform
- Single Hetzner server (Ubuntu 24.04), NetBird node name `zeus`.
- Docker Compose, managed by Colin via the Arcane panel.
- Public exposure via Cloudflare Tunnel (runs as a container) to services on `localhost:<port>`. No ports opened on the host firewall for web apps.
- Identity: Pocket ID is the only OIDC provider. Every web app with a login uses it.
- Internal-only tools (e.g. media stack: media, tor, radarr, sonarr subdomains) are reachable only over NetBird, never via the public tunnel.
- Uptime Kuma monitors services.

## Current services
Pocket ID, NetBird, Arcane, Paperclip (ai.oklepunkt.com, shared instance, critical), AFFiNE, Nextcloud (files.agner.cloud, Wasabi S3), Penpot (design.agner.cloud), media stack (Sonarr, Radarr, Prowlarr, qBittorrent; NetBird-only), Uptime Kuma, Cloudflare Tunnel. The repo is the source of truth; new services may appear.

High risk by definition: Pocket ID, NetBird, Cloudflare Tunnel, Paperclip, Nextcloud storage, backups.

## Repo layout (`agner-cloud-stacks`)
```
<service>/
  compose.yaml
  .env.example      # every variable, placeholder values, comments
  README.md         # runbook (see runbook-writer)
monitoring/checks.md
```
Mirrors `/opt/stacks/<service>/` on the server. One service (plus its own DB/cache) per compose file.

## Compose style
- Pin image tags to a version, never `latest`.
- `restart: unless-stopped`.
- Bind ports to `127.0.0.1:<port>` for tunnel-routed services.
- Named volumes or `./data` bind mounts, documented in the runbook.
- All secrets via `.env`, never inline.
- Healthcheck where the image supports one.
- Container names: `<service>` or `<service>-<component>` (e.g. `papra`, `huly-mongo`).

## Domains
- Public apps: `<name>.agner.cloud`.
- NetBird-only apps: still `<name>.agner.cloud`, but resolved/routed only inside NetBird; state this clearly in the runbook.

## Do not
- Mount the Docker socket into any app unless the issue explicitly requires it and the PR flags it as high risk.
- Introduce Traefik/Nginx Proxy Manager or other reverse proxies; routing is the tunnel's job.
