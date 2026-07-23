# LinkedIn repertoire — post queue

The buffer for IDEAS.md item 1. Two tracks, each roughly weekly. Claude drafts
against `VOICE.md`, Christian voice-checks and posts. Status: `idea` → `drafted`
→ `approved` → `posted (date)`.

**Cadence (agreed 2026-07-12):** journey reports (Track B) go out early in the
week, Monday or Tuesday; leadership stories (Track A) late in the week, Thursday
or Friday. Out so far: B3 Mon 2026-07-13, A1 Thu 2026-07-16, B1 Mon 2026-07-20,
A2 Thu 2026-07-23; next up: B4 (Mon/Tue 2026-07-27/28) and A11 (Thu/Fri
2026-07-30/31).

Harvested 2026-07-12 from all journal entries in `research/`; extended
2026-07-19 (A14–A16, B5) and 2026-07-23 with the 20260721 and 20260723 sessions
(A17–A19, B6–B7).

## Track A — leadership stories (German, du-form)

AI story first (mostly), then the people-leadership translation.

| # | Working title | AI story (source) | Leadership translation | Status |
|---|---|---|---|---|
| A1 | Kontext verloren | Refactoring hit the token limit; compacting failed because the context window was too small; session gone (Christian's own example) | Situational leadership: Christian treated the agent as a senior (delegating) when for this task it was a junior needing telling/selling — smaller goals, checkpoints; match style to task maturity, not to confident appearance (reframed 2026-07-14 from "smaller packages") | posted (2026-07-16, 20260712-li-story-kontextverloren) |
| A2 | Selbstbewusst ist nicht richtig | Agent reasoned confidently about path resolution and was wrong, twice in one session; the empirical check won (20260617) | The most confident voice in the meeting isn't the most correct one; verify at the source instead of trusting delivery style | posted (2026-07-23, 20260718-li-story-selbstbewusst) — repo file reflects the published wording |
| A11 | Ich habe diese Woche jemanden eingestellt | Morten Market hired as marketing agent: goal and task as entry point, deliberately small start with an unknown colleague, explicit clarification, asked Morten himself what he needs for his job (20260718) | Onboarding: trust grows through working together before authority and responsibilities grow; start small with people you don't know yet | drafted, image ready (20260721-li-story-eingestellt) — ready to schedule for Thu/Fri 2026-07-30/31; re-check the closing line after Morten's first scheduled run on Fri 2026-07-25 |
| A19 | Ich wollte im Team sein, nicht darüber | The first team proposal was `agents` — bots only; I renamed it `marketing`, after the work, with Morten and me as its two members, because a team of only bots is a pen, not a team; write access flows through the team (20260723) | The leader who holds responsibility belongs in the team, not above it — equal footing means everyone contributes to the team's goal in good conscience, not to please management | idea (pairs with B7) |
| A20 | Sicherheit und Umkehrbarkeit vor der Veränderung | Characterization tests + a published baseline came before any refactoring and paid off the next session (A3, 20260617/28); both repos were pushed to GitHub *before* a line of rename code, making a risky rewrite reversible (A6, 20260623); and the "simple" rename still touched .gitignore, hardcoded paths, IDE metadata, remote URLs, docs, AI memory, the repo name (A5, 20260624) | Before you demand a big change from a team, make it safe and reversible — psychological safety and two-way doors make people brave — and trace the full chain of references first, because a restructuring touches far more than the org chart | idea (merges A3, A5, A6) |
| A21 | Befähigen, dann beurteilen — was Führung wird | Agents err the way people do, and leading one felt familiar — goal, context, boundaries, feedback, stay in the loop (A7, 20260617/09); delegating only worked once context, goal and boundaries were given first (A8, 20260709); with those in place the website was live in an afternoon, agent doing, human supervising and judging (A9); and well-kept notes turned a later cleanup into minutes — new sessions onboard instantly (A10, 20260622–24) | The leader's value shifts from expertise to judgement — accuracy, impact, risk. Enable before you empower: authority without context is abandonment. And enabling is largely documentation — every new member is a "new session", onboarding quality is documentation quality | idea (merges A7, A8, A9, A10) |
| A22 | Der Brief ist das Problem, nicht die Person | The stats report became genuinely good charts in three attempts once the spec was the audience descriptor "CEO-friendly", not format rules — plus feedback each round (A16, 20260719); and a wrong image was drawn perfectly yet said the opposite of the post because the imageprompt was ambiguous — the fix belonged in the brief, not the worker (A17, 20260721) | Name the audience and the goal, not the method, and let people iterate against feedback. When a result is wrong, question the brief before the worker — assume positive intent; an ambiguous instruction, not bad work, is usually the cause | idea (merges A16, A17; the A17 beat pairs with B6) |
| A23 | Grenzen statt Appelle | Morten concluded himself that the LinkedIn API was closed and still looped API calls until an explicit boundary ("CSV only") stopped him (A14, 20260719); told to open "a new branch", he did better and reused it, so the spec was corrected upward to match (A18, 20260721); and a failing test after an intentional API change raised the real question — which side should move, test or code (A4, 20260628)? | Insight is not behaviour change — explicit boundaries work where appeals to insight don't. When someone beats the instruction, move the rule, not the person. And when reality and a rule collide, decide which side should move instead of gaming the metric | drafted as the A14 beat only (20260723-li-story-grenze, "Er wusste es besser - und tat es trotzdem"), imageprompt ready, for Thu/Fri 2026-08-06/07 to pair with B5 — needs voice-check; PNG pending Morten's next run; the A4 and A18 beats stay unwritten (a single-scene story couldn't carry all three) |
| A24 | Erst prüfen, welche Struktur es wirklich braucht | LinkedIn's native scheduler dissolved half the reminder agent's job before it was built (A13, 20260718); everything for automated stats existed except permission — no analytics API for personal profiles — so a five-minute monthly manual export stayed as a designed process (A15, 20260719); and Morten's channels were defined deliberately — status email for the normal case, Slack to #marketing only when the coming week is empty (A12, 20260718) | Before building a new role or process, check what existing structures already solve — the gap is often smaller than the plan; many walls are institutional, not technical, and a small human ritual can be the better design; and define explicit channels for the normal case versus escalation so the escalation keeps its signal | idea (merges A12, A13, A15) |

Notes on A-track sequencing: A1 is Christian's own pick for the opener. A11
pairs with B4 in the same week (story and report of the same event, like A1/B1
with the token-limit crash). A19 pairs with B7 (part-of-the-team story and the
team-restructure report, same 23.07 event). Among the merged umbrellas, the A17
beat inside A22 pairs with B6 and the A14 beat inside A23 pairs with B5 — so
A22/A23 can still be timed to their reports even though each is now a broader
post. A22 also delivers on A1's published teaser ("über zielorientiertes Führen
und Arbeiten sprechen wir bestimmt auch noch"). A21 is the reflective one; space
it out between story-heavy posts.

**Consolidated 2026-07-23:** the sixteen single-lesson A-ideas were aggregated
into five umbrellas (A20–A24) plus A19 kept standalone, to shrink the queue to
about five open stories. The merged source IDs and their session dates are
preserved in each row's cells, so nothing was lost — each umbrella is one post
that carries several beats.

## Track B — journey reports (English)

Classic "what I did and learned", continuing the published series
(20260617 beginning, 20260618 safety net, 20260709 public snapshot are out).

| # | Working title | Covers | Status |
|---|---|---|---|
| B1 | The big rename | 20260622–20260628 arc: agent hit token limit, so Christian refactored himself in Eclipse (class by class, chasing hardcoded refs e.g. Velocity templates); agent did directories/GitHub repos/cross-checks; publish-before-refactor; missed refs → correct files but broken links/images → characterization tests necessary but not sufficient, content-level tests still to do; 288-file data commit | posted (2026-07-20, 20260718-li-report-bigrename) |
| B2 | The frame keeps widening | 20260709 broadening: agentic → AI, three lenses, "you learn as fast as you build" (partly told in the snapshot post; angle: how the project keeps renaming itself and why that's cheap) | idea |
| B3 | Teaching the AI to sound like me | This session: voice interview, five genuine posts as ground truth, the em-dash confession, building the repertoire itself | posted (2026-07-13, 20260712-li-report-soundlikeme) |
| B4 | Hiring Morten Market | 20260718: the promised reminder agent, hired on Abundly — today he is a queue watchdog and nothing more, but the role is designed to grow into the marketing guy (deliberately small start, trust before authority); spec as versioned repo file (MORTEN.md), public repo as credential-free API between two AI systems, phone-call escalation became Slack (capability gating), agent literacy transferred from Claude to a new platform, a name changed the relationship. Delivers on B1's public "Next up" promise | drafted, image ready (20260721-li-report-hiringmorten) — ready to schedule for Mon/Tue 2026-07-27/28 |
| B5 | Morten's first real job | 20260719: one day after go-live, Morten built PDF statistics reports ad hoc — three rendering attempts (chart.js needs a browser; hand-drawn pie charts came out bulgy; an own JavaScript renderer finally looked right); one API-call loop stopped only by an explicit "CSV only" boundary; the API wall (no analytics API for personal LinkedIn profiles, DMA portability API doubtful, scraping ruled out); decision: manual export as a designed process with monthly reminder — the human as defined interface; spec drift: the Abundly config ran ahead of MORTEN.md for the first time; two agreeing Claudes are correlated answers, not confirmation | drafted (20260723-li-report-firstrealjob), imageprompt ready — for Mon/Tue 2026-08-03/04; needs a voice-check; PNG pending Morten's next run |
| B6 | Morten's first pull request | 20260721: image generation handed to Morten as his second role — he found the two base names needing a PNG, generated both, pushed branch `morten/images-YYYYMMDD`, opened PR #1 and stopped (did not merge); the review gate held on first use but was never tested against resistance; style survived a change of generating model (visual examples beat style text); a wrong image is a wrong prompt — fixed the ambiguous imageprompt in the repo, not just the artifact; he was better than his instructions (reused the branch for the rework → spec corrected upward); fine-grained token as a sharp instrument (Contents + Pull requests = enough to open a PR, not to merge a protected `main`); merge commit over squash to keep his three commits visible; still no identity of his own → IDEAS #19 | idea |
| B7 | Morten becomes a team member | 20260723: `zandercoach` renamed to an org, `chronicler-engine` and this repo transferred in (the "retired repository" wall cleared by GitHub support); a repo transfer silently kills fine-grained tokens — bound to the resource owner, Morten's would have failed unexplained on Friday; onboarded as an org member with his own identity, commits now authored by `morten-market-agent`; team named `marketing` not `agents` (Christian a member, not above it — "a team of only bots is a pen"); permissions made to say what the org chart says (read for all, write via the team, merge via a code-owner review); CODEOWNERS + branch protection make the review gate readable in the repo; for once nothing to mirror to Abundly | idea |

## Parked / raw material

- T-shaped people, smaller-faster teams, authority moving to teams, flatter
  management (20260709 snapshot, org learnings) — thinkpiece, not a story;
  maybe an A-track post once a concrete story carries it.
- "Speed cuts both ways" / balancing doing vs. reflecting (20260618 open
  question) — waiting for the first real speed-induced mess to become a story.
- Two layers of memory, private vs. versioned (20260618) — technical; could
  fold into a B-track report.
- "One event, two audiences, zero extra material" (20260718 other learnings) —
  meta post about the content engine itself; wait until the pattern has
  repeated a few more times. (Now seen five times: A1/B1, A11/B4, the A14 beat
  in A23/B5, the A17 beat in A22/B6, A19/B7 — the pattern has repeated, this one
  is ready to write.)
- "Two agreeing Claudes are comfort, not confirmation" (20260719 other
  learnings) — correlated second opinions; could carry an A-track post about
  consensus vs. confirmation in teams once a human story pairs with it.
