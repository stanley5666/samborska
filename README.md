# websolutions.sk/samborska

Statická prezentácia „Vila Šamborská, Kavečany“. Obsah je v `site/`.

## Nasadenie

Každý push do `main`, ktorý mení `site/`, stránku nahrá cez FTPS. Dá sa spustiť aj ručne: Actions → Deploy → Run workflow.

Nastavenie v GitHube (Settings → Secrets and variables → Actions):

| Typ | Názov | Hodnota |
|---|---|---|
| Secret | `FTP_SERVER` | FTP server hostingu |
| Secret | `FTP_USERNAME` | FTP používateľ |
| Secret | `FTP_PASSWORD` | FTP heslo |

Cieľový priečinok na FTP: `www_root_websolutions_sk/samborska/` (nastavený priamo v workflow).

Ak hosting nepodporuje FTPS, v `.github/workflows/deploy.yml` zmeň `protocol: ftps` na `ftp`.
