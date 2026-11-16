# ACME Updates

Server statico degli aggiornamenti dei plugin WordPress di ACME Studio, pubblicato con GitHub Pages su **https://updates.acmestudio.ch**.

| Plugin | Cartella | Repo sorgente (privata) |
|---|---|---|
| ACME Consent | `acme-consent/` | ACME-Studio-CH/acme-consent-wp |
| ACME Super Admin MCP | `acme-superadmin-mcp/` | ACME-Studio-CH/acme-superadmin-mcp-wp |

Ogni cartella contiene `info.json` (letto dai siti ogni 12 ore) e gli ultimi 5 zip.

**Non modificare a mano**: i file arrivano dalla GitHub Action di rilascio di ogni plugin (tag `vX.Y.Z`), che usa il secret `UPDATES_DEPLOY_TOKEN` con permesso di scrittura solo su questa repo.

La repo è pubblica perché GitHub Pages lo richiede sul piano gratuito: contiene solo i pacchetti dei plugin, nessuna credenziale.

## Configurazione

- Settings > Pages: Deploy from a branch, `main`, `/ (root)`, custom domain `updates.acmestudio.ch`, Enforce HTTPS.
- DNS di acmestudio.ch: `updates` CNAME `acme-studio-ch.github.io`.
