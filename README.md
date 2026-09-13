# oshelpdesk

> A navy/gold theme for osTicket 1.18.x — client portal and staff panel, installed by one idempotent script. For MSPs and self-hosted helpdesks that want an on-brand osTicket without touching PHP.

[![License](https://img.shields.io/github/license/OneByJorah/HelpDeskForge?style=for-the-badge&color=FFB300&labelColor=0a0a09)](https://github.com/OneByJorah/HelpDeskForge)
[![Top Language](https://img.shields.io/github/languages/top/OneByJorah/HelpDeskForge?style=for-the-badge&color=FFB300&labelColor=0a0a09)](https://github.com/OneByJorah/HelpDeskForge)
[![Stars](https://img.shields.io/github/stars/OneByJorah/HelpDeskForge?style=for-the-badge&color=FFB300&labelColor=0a0a09)](https://github.com/OneByJorah/HelpDeskForge/stargazers)
[![Last Commit](https://img.shields.io/github/last-commit/OneByJorah/HelpDeskForge?style=for-the-badge&color=FFB300&labelColor=0a0a09)](https://github.com/OneByJorah/HelpDeskForge/commits)
[![CI](https://img.shields.io/github/actions/workflow/status/OneByJorah/HelpDeskForge/ci.yml?style=for-the-badge&color=FFB300&labelColor=0a0a09)](https://github.com/OneByJorah/HelpDeskForge/actions)

![Client portal with the navy/gold theme applied](docs/screenshots/main.viewport.png)

## What This Is

Stock osTicket looks like stock osTicket. oshelpdesk restyles the 1.18.x support portal and staff panel with a navy/gold identity, delivered as plain CSS and JS plus a bootstrap installer. No osTicket core logic is modified — the installer injects `<link>`/`<script>` tags into the two header includes, so auth, LDAP/AD, and all PHP behavior are untouched.

Both surfaces read colors and spacing from one `theme/css/helpdesk-tokens.css`, so re-skinning the whole deployment means editing a single file.

## Quick Start

```bash
git clone https://github.com/OneByJorah/HelpDeskForge.git && cd oshelpdesk
./deploy.sh /var/www/html   # or omit to clone osTicket v1.18.2 into ./osticket first
```

Point your web server's document root at the target, then hard-refresh with **Ctrl+Shift+R**.

## Features

- **One tokens file** — `helpdesk-tokens.css` drives the palette for both surfaces; rebrand by editing it once.
- **Two skins, both themed** — separate `helpdesk-client-portal.css` and `helpdesk-staff-panel.css` so each side is styled independently.
- **Idempotent installer** — `deploy.sh` marks injections with `HELPDESK-THEME-INJECT` and writes `.bak` backups; safe to re-run.
- **Mobile responsive + dark mode** — the theme adapts to small screens and ships a dark scheme.
- **Standalone previews** — `preview/index.html` and `preview/staff-preview.html` render the theme with no osTicket install, so you can iterate on CSS without a live helpdesk.

## Compatibility

| osTicket | Status |
|---|---|
| 1.18.x (tested v1.18.2) | Fully tested |
| 1.17.x | May need adjustment |
| 1.16.x | Not tested |

## Stack

CSS3, vanilla JavaScript, Bash (installer), osTicket 1.18.x.

## Contributing

Bugs and ideas: [open an issue](https://github.com/OneByJorah/HelpDeskForge/issues). See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT — see [LICENSE](LICENSE).
