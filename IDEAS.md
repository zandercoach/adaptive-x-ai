# Ideas — what to do next

Working backlog for the Adaptive × AI journey. Ordered by horizon; the criterion is **learning about AI's impact per unit of effort**, not output. Sequencing logic: safety net → delegation → organization — the same pattern the journey has already validated twice, applied one level up each time.

Tags: `[eng]` engineering / Chronicler lab · `[showcase]` product & visibility · `[org]` operating model / agent organization · `[lead]` leadership & content · `[disc]` discovery · `[meta]` process

## Now — the next wave

1. **LinkedIn engine: leadership stories + weekly journey reports** `[lead]` ← **starting point**
   Two post tracks, each roughly weekly, to build traction and attention on LinkedIn:
   - *Leadership stories:* transfer learnings from working with agents into real-life leadership stories. Example: ran out of tokens, context window too small to compact current state — everything was lost. Leadership translation: cut work into smaller chunks for overloaded employees.
   - *Journey reports:* the classic "what I did and learned" style, one per week.
   Build a **repertoire** (a buffer of ready posts) plus an **agent that helps get them out periodically**: drafts from journal entries, maintains the queue, reminds when it's time — the final "post" click and voice check stay with Christian. *Why first: Christian's explicit priority; zero infrastructure to start, feeds the repositioning directly, compounds with every journal entry.*

2. **Automated build pipeline (CI/CD) with content tests** `[eng]`
   Runs on check-in, validates and tests, publishes on success. Definitely needs content tests that check the pages' contents, not just the number and names of pages. *Why early: it's the safety net that makes every delegation experiment after it cheap and safe — and verification-without-a-human is itself a core learning.*

3. **Public demo-content repo for the Chronicler** `[showcase]`
   Copyright-free demo RPG content (e.g., `chronicler-data-demo`) to show-case the engine fast, and to serve as a richer test fixture. *Why now: small effort, unlocks three later ideas (demo site, author agent, content tests against public data) and retires the "private for copyright reasons" limitation.*

18. **Let Morten generate the post images** `[org]` `[lead]`
   Today the image step is the only manual break in the drafting chain: Claude Code writes the draft and the imageprompt into the repo, then Christian switches to ChatGPT to generate the flipchart PNG. Claude Code has no image generation; Abundly probably does. Everything Morten would need is already public and versioned — the imageprompt file sits right next to the draft, with the Zander Flipchart style guide at the top. **Decided 2026-07-21, spec written in MORTEN.md:** delivery as a pull request from a `morten/*` branch (not by email, not by pushing to `main`), triggered by the Friday run plus on-demand requests in Slack. Consequences: Morten gets credentials for the first time, `#marketing` becomes a two-way working channel, and a piece of #4 gets pulled forward. Remaining: the setup in GitHub, Slack, and Abundly — plus the open question whether requests and escalations belong in separate channels. *Why now: small, concrete, removes a real friction Christian feels every week — and it's the first step from watchdog toward the co-shaping role of #16.*

19. **A GitHub organization with humans and agents as distinct members** `[org]` `[eng]`
   Two layers of the same question. The *trigger*: the fine-grained token Morten got on 2026-07-21 belongs to Christian's account, so every commit and pull request he makes is authored by "zandercoach" — in the git history his work is indistinguishable from Christian's. The *real move*: set the whole thing up the way a team would be set up — an organization entity holding the repos (`adaptive-x-ai`, `chronicler-engine`, `chronicler-data-cfk`), with humans and agents as separate members, in teams, with roles and permissions per member, and the review gates expressed as org policy rather than per-repo settings. Then every agent that joins later gets onboarded like a colleague instead of borrowing Christian's hands. Investigate: GitHub App vs. machine user per agent, what an org costs at this size, and what moving the repos does to the GitHub Pages site and the custom domain (adaptive-x-ai.org runs from this repo). *Why: if the journey is about working with agents as team members, the tooling should model them as team members — and the history is documentation here, not plumbing. (From the 2026-07-21 session.)*

## Next — delegation

4. **Pull-request infrastructure for agent coding** `[eng]` `[org]`
   Branch protection, agents working on branches, PRs reviewed before merge — maybe set up by an agent itself. Shifts collaboration from side-by-side sessions to asynchronous delegation with review gates.

5. **Modernize the tech stack — as the first fully delegated work** `[eng]`
   Dependencies first (announced as "next up" in the Phase 1 post), potentially the whole stack: outdated libraries, Velocity templates, XML handling, build pipeline. Run it through the PR workflow (#4) as the end-to-end delegation experiment: issue → implementation → tests → PR, human only reviews. *Learning: where trust breaks, and how much review a "finished" delivery really needs.*

6. **Requirements funnel + requirements agent** `[org]`
   One idea in two layers: the *role* — an agent as go-to person for new requirements that asks for clarification, creates backlog entries, and orders them (a bit like what Christian and Claude do interactively now) — and the *plumbing* — input via email, better a chat client or Slack (Claude in Slack exists), landing in a tool (maybe Notion, maybe this repo). *First operating-model experiment outside the codebase.*

16. **Morten Market as a real agent with shared context** `[org]`
   Today Morten is a read-only watchdog on the public repertoire — but he is meant to do marketing, and for that he needs to actively co-shape instead of just watching: contribute ideas, propose queue changes, share context with the Claude Code sessions instead of only reading their output via public raw URLs (a one-way street). What "shared context" between two agents on different platforms should look like is the open design question. *(From the 2026-07-19 session — see the journal's open questions.)*

## Later — organization & showcase

7. **A chronicler agent as ongoing author** `[showcase]` — an agent creating a small but maybe ongoing chronicle of a demo group of heroes and its adventures, published through the engine. Forces the hard agent problems: memory, continuity, quality drift over time. *Depends on: #2.*

8. **Chronicle a real-life project (showcase the engine's abstraction)** `[showcase]` `[org]` — use the engine (Members, Stakeholders, Endeavors) to chronicle a real endeavor. First candidate: this very journey — Christian as member, stakeholders like Ingo, who might join the team later on. *The 2026-06-28 abstraction was the groundwork; this is the payoff.*

9. **Quality agent** `[org]` — keeps track of quality during the development process. *Depends on: experience from #4/#5.*

10. **Dev-architect agent** `[org]` — monitors the whole development process, maybe. *Depends on: experience from #4/#5 and #9.*

11. **Agent org chart for zander.coach** `[org]` — which roles could agents fill (research, marketing ops, training prep), where judgement must stay; then staff one role for real and journal it. *Feeds on: everything learned in #6, #9, #10.*

## Later — discovery lens (deliberately its own wave)

12. **One-day discovery prototype** `[disc]` — prototype a new training-product idea in a single day (e.g., an interactive complexity/AI simulation for workshops) and put it in front of a real client. *Does "validating is cheaper than debating" hold outside code?*

13. **AI on the repositioning interviews** `[disc]` — synthesize customer language from the Jörg/Nina/Miguel interviews, generate candidate hooks, test them as LinkedIn posts. Discovery on the own business.

## Later — content & community

14. **Training module: "Leading agents, leading people — same discipline?"** `[lead]` — the journey becomes product for CSM/leadership trainings. *Wait until enough learnings have accumulated.*
15. **Community talk/session** `[lead]` — Scrum Gathering, Agile Trainers Retreat, SFAO.
17. **Try Substack as a storytelling medium (with newsletter functionality)** `[lead]` `[showcase]` — long-form reports and stories on Substack, teased on LinkedIn. Motivation: LinkedIn feels like a closed shop flooded with generated content, and avoiding vendor lock-in makes sense. A concrete approach still needs to be worked out before starting. *(From the 2026-07-19 session.)*

## Ongoing principles (not backlog items)

- **Balancing doing vs. reflecting** `[meta]` — journal entry per session stays non-negotiable; reflection sections remain handwritten.
- **Site snapshot cadence** `[meta]` — revisit the public page's learnings section roughly monthly, so it stays a living document instead of a launch artifact.
- **Automate repetitive tasks where they hurt** `[meta]` — journal drafting, LinkedIn post creation; fold into #6's funnel thinking rather than building one-offs.

## Dropped / merged

- Spec-driven implementation experiment and XML format migration (Claude proposals) — folded into #5's modernization wave as optional sub-experiments.
- Standalone CI proposal (Claude) — absorbed by #1.
- Time tracking before/after agent support (Claude) — parked; revisit when #11 needs evidence.
