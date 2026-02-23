# ai-ranting
A collection of artifacts for understanding AI and helping others to do the same

## Live pages

| Page | URL |
|------|-----|
| AI Agent Flow | Not yet live — pending DNS setup (see below) |

## Hosting setup

Pages are hosted via **GitHub Pages** on this repo (`RaffaeleT/ai-ranting`), branch `main`.

To enable or change the GitHub Pages configuration:
- Go to **Settings → Pages** on this repo
- Source: `Deploy from a branch`, branch `main`, folder `/ (root)`

The `CNAME` file in the repo root declares the custom domain. Currently set to `www.raffaeleturra.com`.

## Custom domain — current status

The goal is to serve pages at `www.raffaeleturra.com/<page-name>`.

**Blocker:** the `www` subdomain DNS slot is already in use and most DNS providers
only allow one CNAME per hostname. Options to resolve this:

1. **Use a different subdomain** (e.g. `ai.raffaeleturra.com`) — add a CNAME record
   pointing to `raffaelet.github.io`, then update the `CNAME` file in this repo.
2. **Use a `raffaelet.github.io` root repo** — a repo named exactly `raffaelet.github.io`
   is served as the root GitHub Pages site; all other repos become sub-paths automatically
   under the same custom domain.
3. **URL redirect** — if the DNS provider supports HTTP redirects (not just CNAME),
   redirect `www.raffaeleturra.com` to the GitHub Pages URL.

### DNS provider
DNS for `raffaeleturra.com` is managed wherever the domain is registered.
`resume.raffaeleturra.com` is already mapped there as a CNAME to `raffaelet.github.io`
and serves as the reference for how other subdomains should be configured.
