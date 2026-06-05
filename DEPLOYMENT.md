# Deployment notes for aerosmoothlabs.com

This site is deployed through GitHub Pages from:

- Repository: https://github.com/chrisscott617/aerosmoothlabs.com
- Source: `main` branch, repository root
- Custom domain: `aerosmoothlabs.com`

## Porkbun DNS records needed for GitHub Pages

Remove the current parked/forwarding website records for the root and wildcard/www if they conflict with these.

### Root domain (`aerosmoothlabs.com`)

Add these `A` records:

```text
Type: A    Host: @ or blank    Answer: 185.199.108.153    TTL: 600
Type: A    Host: @ or blank    Answer: 185.199.109.153    TTL: 600
Type: A    Host: @ or blank    Answer: 185.199.110.153    TTL: 600
Type: A    Host: @ or blank    Answer: 185.199.111.153    TTL: 600
```

### `www.aerosmoothlabs.com`

Add this `CNAME` record:

```text
Type: CNAME    Host: www    Answer: chrisscott617.github.io    TTL: 600
```

## Keep these email records

Do not delete the Google Workspace records:

- MX: `smtp.google.com`
- SPF TXT: `v=spf1 include:_spf.google.com ~all`
- DKIM TXT at `google._domainkey`
- DMARC TXT at `_dmarc`
- Google site verification TXT

## After DNS updates

1. Wait a few minutes for DNS propagation.
2. Visit `https://aerosmoothlabs.com`.
3. In GitHub repo Settings → Pages, enable **Enforce HTTPS** once GitHub finishes certificate provisioning.
