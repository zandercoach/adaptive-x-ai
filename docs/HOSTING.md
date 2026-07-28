# Hosting & domains

How the public one-page site for the Adaptive × AI journey is hosted and how its
domains are wired. The page itself is `docs/index.html` — plain, self-contained HTML.

## Deployment

- **GitHub Pages**, served from this repo: branch `main`, folder `/docs`.
  `docs/CNAME` pins the custom domain.
- Deployment is **automatic** on push to `main` — no build step. Edit
  `docs/index.html`, commit, push (public repo: commit and push only when asked).
- **The review surface is the live site.** After a push, changes are checked on
  `https://adaptive-x-ai.org` itself, not in a local preview — the live page is the
  single copy, so there is no second version to drift.

## Domains

All three domains are registered at **INWX**.

| Domain | Role | DNS |
|---|---|---|
| `adaptive-x-ai.org` | **Canonical** | Apex `A` → `185.199.108–111.153` (GitHub Pages) + `AAAA`; `www` `CNAME` → `zandercoach.github.io` |
| `adaxai.org` | Redirect alias | INWX "URL" record, `301` → `https://adaptive-x-ai.org` |
| `adaptivexai.org` | Redirect alias | INWX "URL" record, `301` → `https://adaptive-x-ai.org` |

`zandercoach.github.io` is the GitHub **organization** Pages host; the 2026-07-23
repo transfer into the org left Pages intact.

## HTTPS

- Canonical domain: **Let's Encrypt** via GitHub Pages, auto-renewing. "Enforce
  HTTPS" on since 2026-07-09.
- **Caveat on the aliases:** INWX's URL-redirect service has no TLS certificate for
  `adaxai.org` / `adaptivexai.org`, so visiting them over `https://` shows a cert
  warning before the redirect. `http://` and the bare domain are fine. Acceptable
  for now; Cloudflare in front would fix it if it ever matters.

## Legal

zander.coach's Impressum and Datenschutzerklärung explicitly cover
`adaptive-x-ai.org` and both redirect domains, including a GitHub-Pages hosting
section (verified live 2026-07-09). **If the site ever gains anything interactive**
— analytics, a form, an embed — the Datenschutzerklärung needs a matching section
*first*.

## History

- 2026-07-09: site live; all three domains registered; HTTPS enforced.
- 2026-07-23: `zandercoach` became a GitHub organization and the repo moved under
  it; Pages and the domain survived (build green, HTTPS enforced, site returns 200).
  See `research/20260723-morten-becomes-a-team-member.md`.
