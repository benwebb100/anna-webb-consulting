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

## Deploy (GitHub Pages)

1. Push to `main` on GitHub.
2. Repo → Settings → Pages → Source: **Deploy from a branch** → Branch: `main` / root.
3. Site will be available at `https://<user>.github.io/anna-webb-consulting/`.

## Updating content

All copy lives in `index.html`. Update text, the services in the `.offer-grid`, or contact details directly there.
