# 20260728 - The Company Brain and the Team

## What I did

- Set out to fully describe the people on the endeavor — me, Claude, and Morten
  — the way Morten was already described under `agents/`. Sketched a structure,
  then parked it to chase a prior question first.
- Asked how Claude's own knowledge could feed into the single source of truth.
  Claude carries a `CLAUDE.md` and a set of memory files that all live *outside*
  the repo. Audited what was actually in its project memory: six items. Most
  turned out to already be in the repo (the org restructure, the image style),
  so memory was holding duplicate copies that could silently drift.
- Named the discipline instead of just copying memory in: the repo is
  authoritative; memory is only an index into it, plus the two things the repo
  shouldn't hold — Claude's behavioural preferences about working with me, and
  volatile working state. Anything else sitting in memory is a drift risk — the
  same class of bug as Morten's Abundly-config drift and the Slack-vs-repo
  drift, one level up, at the tutor.
- Acted on the audit. Created `docs/HOSTING.md` — the one genuine gap, where the
  DNS records, the domains, the redirect caveat and the legal note had lived
  only in Claude's memory. Promoted the "journal answers as standalone
  statements" convention into `CLAUDE.md`, which is itself versioned in the repo.
  Recorded the posting-date naming rule in `VOICE.md`. Shrank three memory files
  to pointers and deleted the one now covered by `CLAUDE.md`.
- Renamed the framing. `CLAUDE.md` used to open "This repo is Christian's second
  brain." It now opens "our **company brain**" — with the discipline written
  into the same sentence: the shared, reviewed, long-term layer; working state
  stays in each member's private memory. Committed that reframe as its own marked
  commit, then the consolidation as a second, and pushed both.
- Returned to describing the people. Settled on a `team/` directory as the *who*
  layer, distinct from `agents/` — the *how*, a config that only agents have.
  Claude drafted its own entry and Morten's short one; I was interviewed for
  mine, one question at a time.
- My entry, in my own words: I bring the ideas and I'm the one who wants to
  learn — to be back in the game as a player-coach. Corrected Claude's first
  framing of it: I don't relearn how to lead people, I do that all the time as a
  lateral leader wherever I show up. What I relearn is software engineering, and
  doing it with AI — and I want to learn the impact on the business, leadership
  and operating models.
- Claude's entry stayed deliberately honest about how little it is a "member":
  no account, no persistence, working through my identity. I gave it the image
  it now carries — not a team member but my Iron Man suit, a capability I wear,
  powerful in my hands and inert without me in them.
- Linked the three names in the README's "Who works here" into their `team/`
  files, and pushed the roster.

## Technical Learnings

- Memory outside the repo is a second source of truth waiting to drift. The fix
  is not to copy it in wholesale but to classify each item: promote what is
  genuinely project truth, point at what the repo already holds, keep only what
  the repo shouldn't. Most of Claude's "knowledge" turned out to be duplicates —
  the exercise was mostly proving that and cutting the copies.
- The bridge was already there: `CLAUDE.md` is versioned in the repo, so a
  convention about how work is done here doesn't need a new home — moving it into
  `CLAUDE.md` *is* feeding it into the source of truth. The files that correctly
  stay outside (the global `CLAUDE.md`, `ABOUT-ME.md`) are the cross-project and
  personal ones, not journey truth.
- A name can carry a discipline, or lose one. "Company brain" on its own would
  have invited dumping everything back into the repo — the exact drift just
  cleaned up. Attaching the definition (the shared, reviewed layer; working state
  stays private) to the same sentence is what makes the name safe.
- `team/` and `agents/` are two different groupings, not one. `agents/` groups by
  artifact type — versioned configs, which only agents have. `team/` groups by
  roster — a description every member has. Forcing Claude and me into `agents/`
  would have been a fake symmetry: I have no config to version, and Claude's
  isn't its own.
- Describing Claude honestly meant *not* matching Morten. The asymmetry —
  identity, persistence, attribution, whether the boundary is a control or my
  judgment in the moment — is the content, not an awkwardness to smooth over.
  Two agents on one team, at opposite poles of the "tool or team mate" question.

## Organizational Learnings

- The repo becomes the onboarding surface for every new member — and the go-to
  source for company information.

## Leadership Perspective

- I do not really lead a suit like Iron Man. I lead our journey towards our
  vision — and I do that by leading and developing all the company's members,
  humans and agents alike, and by wearing and using this suit myself. For now,
  the members are just Morten.

## Other Learnings

- The company-brain reframe is the standout learning. It is no longer about me
  externalizing my brain to some repo — it is about creating a single source of
  truth for all the people and agents involved.

## Open Questions

- Settled this session: the question carried over from 20260723 — whether Claude
  should get its own identity like Morten did — is answered, and the answer is
  no. The suit framing settles it. Claude is a capability I wear, not a member;
  it does not need an identity of its own.
