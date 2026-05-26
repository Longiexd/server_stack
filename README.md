cd ~/server_stack

# Replace README with clean version
cat > README.md << 'EOF'
# Server Stack

Production infrastructure running on Ubuntu VPS.

## Services

| Service | Domain | Purpose |
|---------|--------|---------|
| **Odoo ERP** | `client01.klynx.net` | Multi-tenant ERP (Docker + Nginx + SSL) |
| **n8n** | `n8n.klynx.net` | Workflow automation |
| **Directus** | `directus.klynx.net` | Headless CMS |

## Architecture


## Tech Stack

- Docker Compose
- Nginx reverse proxy + SSL
- PostgreSQL 15
- Odoo 18
- Let's Encrypt
- Cloudflare

## Notes

- SSL auto-renewal via cron
- Each client has isolated database
- Nginx handles routing and HTTPS
EOF
