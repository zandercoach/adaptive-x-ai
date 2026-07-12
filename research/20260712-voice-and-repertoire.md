# 20260712 - Voice and Repertoire

## What I did

- Started IDEAS.md item 1, the "LinkedIn engine" — with a voice interview before any drafting, at my request: the posts should sound like me, not like an AI.
- Caught a circularity on the way in: the agent's first style profile was inferred from the three published journey posts, which the agent itself had mostly written. Discarded it and rebuilt from ground truth: five genuinely self-written LinkedIn posts as voice samples (LinkedIn blocks automated access to the activity feed; one post was retrievable via a search-indexed public URL, four I pasted in myself).
- Ran the interview one question at a time and wrote the results into `linkedin-posts/VOICE.md`, the binding style guide with the five samples as appendix. Key decisions: leadership stories in German (du-form), journey reports stay English; the classic AI-isms banned and the em-dash rationed to at most two per post; varied, soft, non-clickbait endings; shorter is better; hashtags inline plus new terms at the bottom; emoji sparingly.
- Harvested all eight journal entries into `linkedin-posts/REPERTOIRE.md`: a post queue with 10 leadership-story candidates, 3 journey-report candidates, and parked raw material.
- Drafted the first two posts, each with a flipchart image prompt: the English journey report "teaching the AI to sound like me" (this session's own story) and the first German leadership story "Kontext verloren" (token limit hit during a refactoring, compacting failed because the context window was too small; translation: cut work into smaller packages). I corrected the factual sequence of the context-loss event twice until it matched what actually happened.
- Added two conventions along the way: no external links in the post body (LinkedIn downranks them) — instead the plain phrase "learning journey on adaptive-x-ai" and a paste-ready first-comment block with the URL in every draft file; and a posting cadence: journey reports Monday/Tuesday, leadership stories Thursday/Friday, the report goes first.
- Renamed all files in `linkedin-posts/` so the track is visible in the filename: `YYYYMMDD-li-report-<topic>` / `YYYYMMDD-li-story-<topic>`, dropping the `adaxai` infix for brevity. Committed and pushed in three steps: style guide, repertoire plus drafts, renames.

## Technical Learnings

- Style-modeling has a provenance problem: an AI inferring someone's voice from texts the AI itself drafted converges on itself, not on the person. Check where the "evidence" came from before trusting a profile built on it.
- Encoding voice as a versioned file (hard rules plus genuine samples) turns a subjective "sounds like me" into a checkable artifact — usable by future sessions and, later, by a posting agent, without re-doing the interview.
- LinkedIn blocks automated feed access (HTTP 999), but individual post URLs that search engines have indexed can still be fetched. For a handful of samples, copy-paste by the human was the pragmatic path.
- The best story material was lying in the journal already — 13 post candidates from eight entries. Documentation written for one purpose (reflection) turned out to be the raw material for another (content).
- PowerShell 5.1 quirk: a multi-line commit message in a here-string broke when it contained double quotes — git received the message in fragments. Writing the message to a file and using `git commit -F` is the robust route.
- `git mv` keeps file history intact (100% similarity detection), so a naming-convention change across 13 files is cheap. A filename should carry the distinction you actually need at a glance — the speaking words `report`/`story` beat cryptic track letters.

## Organizational Learnings

- Part of my external communication now has a defined, semi-automated process with a queue and a cadence — where it used to happen ad hoc.
- Plannable and repeatable work can be handed to agents. But the human is still in charge and needs to stay in the loop — it's less about doing, more about judging, again. And someone still has to know HOW things work, so that they can fix things when AI can't. I think it's going to be some kind of balance: doing things yourself to not forget how they work, and handing the tedious things over to AI to become more efficient.

## Leadership Perspective

- REPERTOIRE.md now contains ideas for LinkedIn posts. The goal was and is to automate the creation process of posts while still being in charge and in the loop as a human. VOICE.md defines a clear boundary to create posts in my style. Goals and clear boundaries are also needed when empowering individuals or teams — otherwise teams work with no direction and/or do whatever they see fit.
- I had to correct the facts twice — reviews remain the boss's job in my learning journey.

## Other Learnings

- Your own voice needs active protection. The AI imitated my style well enough that it could have passed as mine — the difference only became visible in comparison with genuine samples. Authenticity isn't something that stays by itself; it's something to curate, with ground truth written by your own hand.
- The journey produces its own content. The session about the post process itself delivered the next post — the journey report tells exactly this story. As with the site launch: when you learn in public, the method is the exhibit.
- Old material gains new value. Five old LinkedIn posts, written without any thought of AI, were the most valuable input of the day. Personal archives — posts, flipcharts, notes — are suddenly training material for your own agents: keeping them, and keeping them findable, pays off.

## Open Questions

- How will the agent remind me when a post is due?
