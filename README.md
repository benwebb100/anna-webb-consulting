# Anna Webb Consulting

Marketing site for Anna Webb — executive coach, leadership development consultant and facilitator (Melbourne, Australia).

## Structure

- `index.html` — single-page site (Home · About · What we offer · Contact)
- `styles.css` — all styling
- `script.js` — mobile nav toggle + footer year
- `images/` — hero and about portraits

## Local preview

Open `index.html` directly in a browser, or run a quick static server:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Deploy (Render)

Hosted on [Render](https://render.com) as a static site: service `anna-webb-consulting` → https://anna-webb-consulting.onrender.com. Render auto-deploys `main` of `benwebb100/anna-webb-consulting`. There's no build step (the repo root is served as-is), so pushing to `main` is the deploy.

### Domain and DNS

**annawebb.com.au** is the canonical domain; `www` 301-redirects to it. Render issues and renews the SSL certificate. DNS is managed at VentraIP (VIP Control), not at Render.

| Record | Type | Value | For |
|---|---|---|---|
| `annawebb.com.au` | A | `216.24.57.1` | Website (Render) |
| `www.annawebb.com.au` | CNAME | `anna-webb-consulting.onrender.com` | Website (Render) |
| `annawebb.com.au` | MX | `mail.annawebb.com.au` | Email (VentraIP) |
| `mail.annawebb.com.au` | A | `43.250.140.27` | Email (VentraIP) |

**Email stays on VentraIP. Never repoint the MX or mail records at Render.** Render runs no mail server, so pointing the MX record, `mail.annawebb.com.au` or the cPanel service records (webmail, autodiscover, autoconfig, cpanel, …) at Render would stop anna@annawebb.com.au receiving mail. Only the apex A record and the `www` CNAME belong to Render.

## Updating content

All copy lives in `index.html`. Update text, the services in the `.offer-grid`, or contact details directly there.
