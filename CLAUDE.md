# Instructions for Claude Code working in this repo

This repo is **our company brain** for the "Adaptive × AI" learning journey (see README.md for the why): the shared, versioned source of truth that everyone on the team — human and agent — reads from and can rely on. It is the *long-term, reviewed* layer of that brain — durable facts, decisions, conventions and the journal — not a place for working state. Each member keeps their own private working memory outside the repo (Claude's session memory, Morten's Abundly context); only what is reviewed and shared belongs here. It documents the *journey*, not the code — the actual project being modernized along the way lives in separate repos (`chronicler-engine`, the public engine, and `chronicler-data-cfk`, the private content).

## Structure

- `research/YYYYMMDD-topic.md` — one entry per session or topic, oldest first by filename.
- Each entry uses this template, in this order:
  1. `## What I did` — factual recap of what happened in the session.
  2. `## Craft` — technical and process lessons; the hands-on layer.
  3. `## Business Model` — what AI changes about what is built and sold, and about what a value proposition is worth.
  4. `## Leadership Model` — leading people and agents; judgement, trust, accountability.
  5. `## Operating Model` — how work is organized, teams are structured, decisions flow.
  6. `## Other Learnings` — anything that doesn't fit the categories above.
  7. `## Open Questions` — what's still unresolved.
- **A section with nothing in it is left out, not left empty.** Not every session
  touches all three models; a heading with an invented line under it is worse than
  a missing heading.
- The three models are the working hypothesis (see README.md), and `RESOURCES.md`
  sorts sources by the same four names — so an entry and a source can be held
  against each other.
- **Entries up to and including `20260905` use the earlier headings**
  (`Technical Learnings`, `Organizational Learnings`, `Leadership Perspective`).
  They are records of their moment and stay as they are; nothing is converted
  retroactively.

## Filling in an entry

`What I did` and `Craft` can be drafted directly from session history — they're factual and observable.

**`Craft` holds four bullets at most.** A session yields two or three lessons that
matter; a list of eight buries them. Keep what changed how the work is done, drop
what merely happened — that is what `What I did` is for.

**Keep `What I did` short as well**, though without a fixed number: a recap of the
session, not a transcript of it. Christian writes shorter than an agent does by
default, and the entry should read like his.

The rest (`Business Model`, `Leadership Model`, `Operating Model`, `Other Learnings`, `Open Questions`) is Christian's personal reflection. **Never invent or paraphrase these from inference alone.** Ask him directly, one question at a time, waiting for his answer before asking the next. Write his answers close to his own words — light cleanup for readability is fine, rewriting his voice is not.

When you write his answer into a reflection section, make it a **self-contained statement, not a reply.** Drop the conversational opener ("Both, actually", "Yes, because…") and put back the thing it refers to, so the bullet stands on its own when the entry is read later without the interview around it. Everything after the opener stays close to his words. E.g. "Both at once" becomes "Giving write access was both at once — giving trust and installing a safeguard — and the safeguard is what made the trust cheap."

## The public site

`docs/index.html` and `docs/resources.html` describe **the current state only.** History belongs in the journal — that is what `research/` is for. Nothing on the site was designed up front; what it shows is the current result of an evolution through learning, and the path there — including the wrong turns — is the journal's job to carry. The site says as much in its "Follow along" section, so a reader knows a snapshot is what they are reading.

- Do not narrate how something came to be: no "it was first called X, then became Y", no reasoning for alternatives that were rejected. When a change lands, rewrite the affected passage as if the new state had always been the case.
- Principles and commitments stay, because they are current ("no second team", "the one holding the responsibility belongs inside the team"). The story that produced them goes. Keep reasoning only where it explains a *present* design, not a past decision.
- Watch for stale time markers — "since this week", "as of today" — they date the page silently as it ages.
- The journal has the opposite rule: entries are immutable records of their moment (see below). Together the two make the site a living snapshot and `research/` the archive; neither has to do the other's job.

## Working in this repo

- Before updating or referencing an entry, read its current file content — don't rely on memory of what it used to say, since it changes across sessions and may have been edited directly (by Christian or a linter) between sessions.
- New entries follow the template above — same headings, same order, minus whatever a session gave nothing for — unless Christian asks to change the template itself.
- Commit only when explicitly asked. Push only when explicitly asked — this is a public repo.
