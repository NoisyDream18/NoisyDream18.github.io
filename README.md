# NoisyDream18.github.io

Personal portfolio site. Dark-technical aesthetic. Zero frameworks, zero build step — pure HTML, CSS, and JS.

Live at → **https://NoisyDream18.github.io**

## File structure

```
.
├── index.html                  ← main page (edit this)
├── assets/
│   ├── css/main.css            ← all styles + CSS custom properties
│   └── js/main.js              ← grid canvas, scroll reveal, nav highlight
├── images/
│   ├── favicon.svg             ← SVG favicon (edit the text inside)
│   └── og-image.png            ← add your own 1200×630 for link previews
├── CNAME                       ← custom domain (commented out)
└── .github/
    └── workflows/
        └── deploy.yml          ← auto-deploy on push to main
```

## Quick start

### 1. Enable GitHub Pages

Go to your repo → **Settings → Pages → Source → GitHub Actions**.

The `deploy.yml` workflow fires on every push to `main` and deploys automatically.

### 2. Customize index.html

Global find-replace on these strings:

| Find | Replace with |
|---|---|
| `you@example.com` | your actual email |
| `yourhandle` | your LinkedIn handle |
| `add handle` | your LinkedIn handle |
| `interest_1, interest_2, interest_3` | your actual interests |
| Edit project cards directly | fill in real titles, descriptions, stack, links |

### 3. Tune the design

All colors live in `assets/css/main.css` under `:root { ... }`.
Key variables: `--acc` (cyan accent), `--bg`, `--text`, `--border`.

### 4. Add OG image

Drop a `1200×630` PNG at `images/og-image.png` for rich link previews on social/Discord.

### 5. Custom domain (optional)

Edit `CNAME` — uncomment the line and replace with your domain:
```
jack-west.com
```
Then configure DNS per [GitHub's docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Local preview

No build needed — just serve the directory:

```bash
python3 -m http.server 8080
# or
npx serve .
```

Then open http://localhost:8080.

## What to replace / delete

The repo previously had a Jekyll scaffold (`Gemfile`, `Gemfile.lock`, `_config.yml`, `index.md`).
**Delete all of those** — they're listed in `.gitignore` as a reminder.
This site is plain static; Jekyll is not needed.
