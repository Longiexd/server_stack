Production infrastructure running on Ubuntu VPS.

## Services

| Service | Domain | Purpose |
|---------|--------|---------|
| **Odoo ERP** | `client01.klynx.net` | Multi-tenant ERP (Docker + Nginx + SSL) |
| **n8n** | `n8n.klynx.net` | Workflow automation |
| **Directus** | `directus.klynx.net` | Headless CMS |

## Architecture


## Key Features

- **Multi-tenancy** — Isolated databases per client
- **SSL Automation** — Let's Encrypt with auto-renewal via cron
- **Reverse Proxy** — Nginx routes domains to correct containers
- **Health Checks** — PostgreSQL containers verify readiness before Odoo starts
- **Persistent Volumes** — Data survives container restarts

## Tech Stack

- Docker Compose
- Nginx (Alpine)
- PostgreSQL 15
- Odoo 18
- Let's Encrypt / Certbot
- Cloudflare DNS
- Ubuntu 22.04 LTS


## Notes

- SSL auto-renewal via cron
- Each client has isolated database
- Nginx handles routing and HTTPS
