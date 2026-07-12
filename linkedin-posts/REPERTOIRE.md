# LinkedIn repertoire — post queue

The buffer for IDEAS.md item 1. Two tracks, each roughly weekly. Claude drafts
against `VOICE.md`, Christian voice-checks and posts. Status: `idea` → `drafted`
→ `approved` → `posted (date)`.

**Cadence (agreed 2026-07-12):** journey reports (Track B) go out early in the
week, Monday or Tuesday; leadership stories (Track A) late in the week, Thursday
or Friday. First up: B3 (Mon/Tue 2026-07-13/14), then A1 (Thu/Fri 2026-07-16/17).

Harvested 2026-07-12 from all journal entries in `research/`.

## Track A — leadership stories (German, du-form)

AI story first (mostly), then the people-leadership translation.

| # | Working title | AI story (source) | Leadership translation | Status |
|---|---|---|---|---|
| A1 | Kontext verloren | Refactoring hit the token limit; compacting failed because the context window was too small; session gone (Christian's own example) | Cut work into smaller chunks for overloaded employees; an overloaded person can't even hand over properly | drafted (20260712-li-story-kontextverloren) |
| A2 | Selbstbewusst ist nicht richtig | Agent reasoned confidently about path resolution and was wrong, twice in one session; the empirical check won (20260617) | The most confident voice in the meeting isn't the most correct one; verify at the source instead of trusting delivery style | idea |
| A3 | Erst das Netz, dann die Kür | Characterization tests and a published baseline came before any refactoring; paid off the very next session (20260617, 20260628) | Build safety before demanding change from a team; psychological safety and reversibility make people brave | idea |
| A4 | Wer muss sich bewegen? | Test fails after an intentional API change: first question is not "how do I make it pass?" but "which side should move — test or code?" (20260628) | When reality and a rule/KPI/process collide, ask which side should move instead of gaming the metric | idea |
| A5 | Der Preis eines neuen Namens | A "simple" directory rename touched .gitignore, hardcoded paths, IDE metadata, remote URLs, docs, AI memory, repo name (20260624) | Renaming a team or restructuring touches far more than the org chart; trace the full chain of references before declaring it done | idea |
| A6 | Veröffentlichen vor dem Umbau | Pushed both repos to GitHub *before* writing a single line of rename code, turning a risky rewrite into a reversible operation (20260623) | Make big changes reversible before you start them; two-way doors let teams move fast without fear | idea |
| A7 | Fehler wie ein Mensch | Agents make mistakes the way people do; leading one felt familiar: goal, context, boundaries, feedback, stay in the loop (20260617, 20260709) | Coaching vocabulary transfers to agents — and back: the discipline of leading is the same | idea |
| A8 | Befähigen vor Ermächtigen | Delegating to an agent only works when context, goal, and boundaries are provided first (20260709 snapshot) | Enable teams before empowering them: authority without context is abandonment | idea |
| A9 | Vom Machen zum Beurteilen | Website live in one afternoon: agent did the doing, human supervised, reviewed, adjusted; judgement over know-how (20260709 snapshot) | The leader's value shifts from expertise to judgement: accuracy, impact, risk | idea |
| A10 | Dokumentation ist plötzlich fast gratis | Well-kept notes turned a later cleanup from archaeology into minutes; new sessions onboard instantly from good docs (20260622–24) | Onboarding quality is documentation quality; every new team member is a "new session" | idea |

Notes on A-track sequencing: A1 is Christian's own pick for the opener. A2/A3
are the strongest stories (concrete failure, concrete payoff). A8/A9 are more
reflective; space them out between story-heavy posts.

## Track B — journey reports (English)

Classic "what I did and learned", continuing the published series
(20260617 beginning, 20260618 safety net, 20260709 public snapshot are out).

| # | Working title | Covers | Status |
|---|---|---|---|
| B1 | The big rename | 20260622–20260628 arc: reframe, publish-before-refactor, downstream reference chains, "which side should move", 288-file data commit | idea |
| B2 | The frame keeps widening | 20260709 broadening: agentic → AI, three lenses, "you learn as fast as you build" (partly told in the snapshot post; angle: how the project keeps renaming itself and why that's cheap) | idea |
| B3 | Teaching the AI to sound like me | This session: voice interview, five genuine posts as ground truth, the em-dash confession, building the repertoire itself | drafted (20260712-li-report-soundlikeme) |

## Parked / raw material

- T-shaped people, smaller-faster teams, authority moving to teams, flatter
  management (20260709 snapshot, org learnings) — thinkpiece, not a story;
  maybe an A-track post once a concrete story carries it.
- "Speed cuts both ways" / balancing doing vs. reflecting (20260618 open
  question) — waiting for the first real speed-induced mess to become a story.
- Two layers of memory, private vs. versioned (20260618) — technical; could
  fold into a B-track report.
