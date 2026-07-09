# 20260709 - Public Snapshot Live

## What I did

- Decided to publish a first public snapshot of this learning journey: a one-page site describing the intention, the process, and the first learnings — minimal design, curious-but-experienced tone, a bit ironic.
- Checked candidate domains for availability via RDAP, picked `adaptive-x-ai.org` as the canonical domain with `adaxai.org` as a short alias, and registered both at INWX (chosen deliberately: German registrar, domains as core business, flat renewal pricing, solid DNS panel). Later grabbed `adaptivexai.org` as a third domain and set it up as another alias.
- Drafted the site as a single self-contained `docs/index.html`: no framework, no build step, no webfonts — system serif for the essay voice, monospace for the metadata voice, one verdigris accent (a nod to the cauldron), light and dark theme. The six "first learnings" were distilled from the seven journal entries so far; the reflection-derived ones stay close to my own words.
- Iterated the copy and layout: added the "late to the AI party — at least to the part that goes beyond prompting" line, enlarged the headlines, and widened the text column.
- Went live: committed and pushed `docs/` (index.html + CNAME), enabled GitHub Pages (branch `main`, folder `/docs`), configured INWX DNS (four A + four AAAA records on the apex, `www` CNAME to `zandercoach.github.io`, URL-redirect records with 301 for both alias domains).
- Verified each step empirically with `nslookup` and `curl`: DNS propagation, page serving, redirect chains, Let's Encrypt certificate issuance. Enabled "Enforce HTTPS" via the GitHub API once the certificate arrived; a triggered Pages rebuild made the http→https redirect take effect.
- Extended the zander.coach Impressum and Datenschutzerklärung to cover the new domains: a scope statement on both pages plus a GitHub-Pages hosting section (server logs, Art. 6 Abs. 1 lit. f DSGVO, no cookies/tracking on the site itself). Verified the live pages afterwards.

## Technical Learnings

- RDAP makes domain-availability checks scriptable: `rdap.org/domain/<name>` answers 404 for unregistered domains — eight candidates checked in one loop, no registrar UI needed.
- A fully self-contained static page (system font stacks, inline SVG favicon, inline CSS, no build) makes hosting almost free of moving parts: GitHub Pages needed only a `CNAME` file and one settings change.
- A custom-domain go-live is a fixed dependency chain — push CNAME → enable Pages → DNS records → GitHub's DNS check → certificate issuance → Enforce HTTPS — and every link in the chain is observable with `nslookup`/`curl` instead of waiting blind. The same verify-don't-assume discipline from the code sessions applies to infrastructure.
- Enabling "Enforce HTTPS" via API didn't propagate on its own; triggering a Pages rebuild did. Some cloud-side state needs a nudge, and only observation tells you whether the setting is actually live.
- INWX's URL-redirect DNS record type handles alias domains without any hosting, but serves no TLS certificate for the alias — `https://adaxai.org` typed directly warns. Acceptable for a short alias; moving the alias DNS to Cloudflare would be the fix if it ever matters.
- Going public has a legal leg, not just a technical one: extending the existing zander.coach Impressum/Datenschutzerklärung with a scope statement was far cheaper than separate pages, and a static site without cookies or third-party embeds needs no consent banner — only a hosting/logfiles passage.

## Organizational Learnings

- With the help of AI, capable people will become even more capable — as long as they can make fair judgements of the task at hand, the context, the boundaries, and the goal provided. They will become more T-shaped, assisted by an agent that can provide knowledge around how to do things. So technical expertise might become an AI domain, while reasoning and judgement remain in human hands — yes: not black-and-white.
- Most likely, this will have an impact on teams working in product engineering as well as other areas. As communication becomes clearer and more precise (due to working with agents), and clear and precise documentation becomes a helpful side-effect, humans profit as well. But it also means teams can rely on the help of agents with extensive expertise — so teams will get faster, although maybe smaller. As those teams can and will make faster yet better decisions, authority will move to the teams. This in turn will have an impact on the "manager" side of an organization — most likely flatten it...

## Leadership Perspective

- A new (simple) website under a newly registered URL with a new provider — all in one go. The work shifts from doing to supervising, reviewing, and adjusting. So understanding context and decisions will become more important than actually knowing where to find what or how to do stuff. Judgement — with regards to the accuracy of information and to the impact and risk of decisions — will become more important in the future.
- As a leader, I need to enable teams and individuals to make decisions by providing context — enabling them before empowering them.

## Other Learnings

- Going public changes the stakes. The moment the journal got a URL, it acquired a legal surface (Impressum, Datenschutz) and a reputational one (tone, irony calibration). A repo is notes; a domain is a statement.
- The site is its own first exhibit. A page about learning what AI changes about work was itself produced the new way — one afternoon, human judgement plus agent execution. Whoever reads it is looking at the method, not just a description of it.

## Open Questions

- None right now.

