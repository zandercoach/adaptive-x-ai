# LinkedIn repertoire — post queue

The buffer for IDEAS.md item 1. Two tracks, each roughly weekly. Claude drafts
against `VOICE.md`, Christian voice-checks and posts. Status: `idea` → `drafted`
→ `approved` → `posted (date)`.

**Cadence (agreed 2026-07-12):** journey reports (Track B) go out early in the
week, Monday or Tuesday; leadership stories (Track A) late in the week, Thursday
or Friday. Out so far: B3 Mon 2026-07-13, A1 Thu 2026-07-16, B1 Mon 2026-07-20;
next up: A2 (Thu/Fri 2026-07-23/24), then B4 (Mon/Tue 2026-07-27/28) and A11
(Thu/Fri 2026-07-30/31).

Harvested 2026-07-12 from all journal entries in `research/`.

## Track A — leadership stories (German, du-form)

AI story first (mostly), then the people-leadership translation.

| # | Working title | AI story (source) | Leadership translation | Status |
|---|---|---|---|---|
| A1 | Kontext verloren | Refactoring hit the token limit; compacting failed because the context window was too small; session gone (Christian's own example) | Situational leadership: Christian treated the agent as a senior (delegating) when for this task it was a junior needing telling/selling — smaller goals, checkpoints; match style to task maturity, not to confident appearance (reframed 2026-07-14 from "smaller packages") | posted (2026-07-16, 20260712-li-story-kontextverloren) |
| A2 | Selbstbewusst ist nicht richtig | Agent reasoned confidently about path resolution and was wrong, twice in one session; the empirical check won (20260617) | The most confident voice in the meeting isn't the most correct one; verify at the source instead of trusting delivery style | approved — scheduled in LinkedIn for Thu/Fri 2026-07-23/24 (20260718-li-story-selbstbewusst) |
| A3 | Erst das Netz, dann die Kür | Characterization tests and a published baseline came before any refactoring; paid off the very next session (20260617, 20260628) | Build safety before demanding change from a team; psychological safety and reversibility make people brave | idea |
| A4 | Wer muss sich bewegen? | Test fails after an intentional API change: first question is not "how do I make it pass?" but "which side should move — test or code?" (20260628) | When reality and a rule/KPI/process collide, ask which side should move instead of gaming the metric | idea |
| A5 | Der Preis eines neuen Namens | A "simple" directory rename touched .gitignore, hardcoded paths, IDE metadata, remote URLs, docs, AI memory, repo name (20260624) | Renaming a team or restructuring touches far more than the org chart; trace the full chain of references before declaring it done | idea |
| A6 | Veröffentlichen vor dem Umbau | Pushed both repos to GitHub *before* writing a single line of rename code, turning a risky rewrite into a reversible operation (20260623) | Make big changes reversible before you start them; two-way doors let teams move fast without fear | idea |
| A7 | Fehler wie ein Mensch | Agents make mistakes the way people do; leading one felt familiar: goal, context, boundaries, feedback, stay in the loop (20260617, 20260709) | Coaching vocabulary transfers to agents — and back: the discipline of leading is the same | idea |
| A8 | Befähigen vor Ermächtigen | Delegating to an agent only works when context, goal, and boundaries are provided first (20260709 snapshot) | Enable teams before empowering them: authority without context is abandonment | idea |
| A9 | Vom Machen zum Beurteilen | Website live in one afternoon: agent did the doing, human supervised, reviewed, adjusted; judgement over know-how (20260709 snapshot) | The leader's value shifts from expertise to judgement: accuracy, impact, risk | idea |
| A10 | Dokumentation ist plötzlich fast gratis | Well-kept notes turned a later cleanup from archaeology into minutes; new sessions onboard instantly from good docs (20260622–24) | Onboarding quality is documentation quality; every new team member is a "new session" | idea |
| A11 | Ich habe diese Woche jemanden eingestellt | Morten Market hired as marketing agent: goal and task as entry point, deliberately small start with an unknown colleague, explicit clarification, asked Morten himself what he needs for his job (20260718) | Onboarding: trust grows through working together before authority and responsibilities grow; start small with people you don't know yet | drafted, image ready (20260721-li-story-eingestellt) — ready to schedule for Thu/Fri 2026-07-30/31; re-check the closing line after Morten's first scheduled run on Fri 2026-07-25 |
| A12 | Wann darf dein Team dich anrufen? | Morten's channels: weekly status email (normal case), Slack to #marketing only if the coming week is empty (escalation); distributed setup — Christian at home, Morten in Sweden (20260718) | Explicit communication channels for normal and escalation cases prevent misunderstandings and alarm fatigue — vital for distributed teams across locations, countries, time zones | idea |
| A13 | Der halbe Job verschwand beim Hinsehen | LinkedIn's native scheduler dissolved half the reminder agent's job before it was built; the remaining job was smaller and better defined (20260718) | Before creating a new role or process, check what existing structures already solve; the real gap is often smaller than the plan | idea |
| A14 | Er wusste es - und tat es trotzdem | Morten concluded himself that the LinkedIn API route was closed — and still fell into a loop of API calls in the very next attempt, until an explicit boundary ("no API calls, CSV only") stopped him (20260719) | Insight is not behavior change: people also know better and still fall back into old patterns; explicit agreements and boundaries work where appeals to insight don't | idea |
| A15 | Die Mauer war nicht technisch | Everything for automated LinkedIn statistics existed — data, agent, channels — except permission: no analytics API for personal profiles; kept a five-minute-per-month manual export as a designed process instead (20260719) | Blockers in organizations are often institutional, not technical; weigh cost and benefit honestly — sometimes a small human ritual is the better design than fragile automation | idea |
| A16 | „CEO-friendly" statt Formatvorgaben | The stats report went from tables-tables-tables to genuinely good charts in three attempts; the effective specification was the audience descriptor "CEO-friendly", not detailed format requirements — plus feedback per iteration (20260719) | Name the audience and the goal, not the method; let people (and agents) iterate against feedback instead of prescribing the path | idea |

Notes on A-track sequencing: A1 is Christian's own pick for the opener. A2/A3
are the strongest stories (concrete failure, concrete payoff). A8/A9 are more
reflective; space them out between story-heavy posts. A11 pairs naturally with
B4 in the same week (story and report of the same event, like A1/B1 with the
token-limit crash). A11 overlaps thematically with A8 (enable before empower)
— don't run them back to back. A14 pairs with B5 in the same week (story and
report of the same event — third instance of that pattern after A1/B1 and
A11/B4). A16 delivers on A1's published teaser ("über zielorientiertes Führen
und Arbeiten sprechen wir bestimmt auch noch"). A15 and A13 share the
"check reality before building" family — space them out.

## Track B — journey reports (English)

Classic "what I did and learned", continuing the published series
(20260617 beginning, 20260618 safety net, 20260709 public snapshot are out).

| # | Working title | Covers | Status |
|---|---|---|---|
| B1 | The big rename | 20260622–20260628 arc: agent hit token limit, so Christian refactored himself in Eclipse (class by class, chasing hardcoded refs e.g. Velocity templates); agent did directories/GitHub repos/cross-checks; publish-before-refactor; missed refs → correct files but broken links/images → characterization tests necessary but not sufficient, content-level tests still to do; 288-file data commit | posted (2026-07-20, 20260718-li-report-bigrename) |
| B2 | The frame keeps widening | 20260709 broadening: agentic → AI, three lenses, "you learn as fast as you build" (partly told in the snapshot post; angle: how the project keeps renaming itself and why that's cheap) | idea |
| B3 | Teaching the AI to sound like me | This session: voice interview, five genuine posts as ground truth, the em-dash confession, building the repertoire itself | posted (2026-07-13, 20260712-li-report-soundlikeme) |
| B4 | Hiring Morten Market | 20260718: the promised reminder agent, hired on Abundly — today he is a queue watchdog and nothing more, but the role is designed to grow into the marketing guy (deliberately small start, trust before authority); spec as versioned repo file (MORTEN.md), public repo as credential-free API between two AI systems, phone-call escalation became Slack (capability gating), agent literacy transferred from Claude to a new platform, a name changed the relationship. Delivers on B1's public "Next up" promise | drafted, image ready (20260721-li-report-hiringmorten) — ready to schedule for Mon/Tue 2026-07-27/28 |
| B5 | Morten's first real job | 20260719: one day after go-live, Morten built PDF statistics reports ad hoc — three rendering attempts (chart.js needs a browser; hand-drawn pie charts came out bulgy; an own JavaScript renderer finally looked right); one API-call loop stopped only by an explicit "CSV only" boundary; the API wall (no analytics API for personal LinkedIn profiles, DMA portability API doubtful, scraping ruled out); decision: manual export as a designed process with monthly reminder — the human as defined interface; spec drift: the Abundly config ran ahead of MORTEN.md for the first time; two agreeing Claudes are correlated answers, not confirmation | idea |

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
  repeated a few more times. (Now seen three times: A1/B1, A11/B4, A14/B5 —
  getting close.)
- "Two agreeing Claudes are comfort, not confirmation" (20260719 other
  learnings) — correlated second opinions; could carry an A-track post about
  consensus vs. confirmation in teams once a human story pairs with it.
