# AeroSmooth Labs website

Static company website for `aerosmoothlabs.com`.

## Local preview

```bash
cd sites/aerosmoothlabs
python3 -m http.server 4173
```

Open `http://127.0.0.1:4173`.

## Pages

- `/` — company landing page
- `/btrd.html` — btrd product page
- `/support.html` — support/contact page
- `/privacy.html` — privacy policy

## Deployment notes

This is a dependency-free static site. It can be served by Caddy, Nginx, GitHub Pages, Cloudflare Pages, Netlify, Vercel, or Porkbun static hosting.
