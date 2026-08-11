# 20260812 - Morten Takes the Harvest

## What I did

- Decided to hand the LinkedIn post work to Morten: harvest candidates from every
  new journal entry into `REPERTOIRE.md`, and draft both posts of the coming week
  on Friday mornings with two image proposals each, one pull request per post. Set
  the target as *Morten drafts, I finish* — the argument that turns a draft into a
  post stays with me, it only moves out of the Claude Code session and into the
  pull request review.
- Had the plan checked against what Morten actually has today, and learned that
  the file-type limit in his instructions — "only image files, never text files,
  drafts, specs, or the journal" — was never a control. Branch protection and
  CODEOWNERS are; the file-type rule lived only in the instruction block, and his
  token could always write text. The handover needed no new access at all.
- Decided Morten writes his own `-imageprompt.txt` from now on, because he
  identifies the post's goal while drafting it, so the brief and the draft come
  out of the same reading.
- Took the incremental route instead of a big-bang handover, and found the
  schedule already sitting in the calendar: the queue is scheduled through 20.08,
  so the coming week is fully occupied on the 14.08 run and the first drafting run
  cannot happen before 21.08. Stage 1 is the harvest from 14.08; stage 2 is the
  Track B slot on 21.08 with the story still drafted in a session; stage 3 is both
  tracks from 28.08.
- Answered three design questions one at a time. I review alone — Claude Code does
  not read Morten's pull requests before I do, because the argument for it was
  that Claude sat in the sessions the entries describe, and that is session memory
  acting as a second source of truth. Morten appends new rows and names merge
  candidates rather than merging them himself. The Friday run is the trigger
  rather than an event on push.
- Shipped the harvest stage: the workflow, the boundary rewritten from "only image
  files" into an explicit two-file allowlist, a machine-readable harvest watermark
  in `REPERTOIRE.md` set to `20260801-catching-up-the-record.md`, the team roster,
  and IDEAS #1, #16, #21 and #22 updated.
- Promoted the two requests the goal-oriented image briefs had carried — say so
  instead of guessing, and write down which idea you chose and why — out of brief
  text and into standing instructions covering every job. They would otherwise
  have disappeared together with the last hand-written brief.
- Mirrored to Abundly and ran a dry run. Morten harvested from 20260801 on and
  showed what the pull request would look like.
- Got his first finding back out of that dry run: he cannot hold the "about five
  open ideas per track" rule while being forbidden to touch existing rows. Gave
  the count to myself — harvest only ever adds, consolidation stays my own pass —
  and wrote in explicitly that he must never leave a candidate out to keep a
  number, because too many rows is a review that takes a minute and too few is
  invisible.
- Mirrored that fix and had him read his own specification. He came back with
  three findings. The Friday order was impossible: the image workflow has said
  "mention the pull request in your Friday email" since 21.07 while running after
  the report that email is. The Friday specification existed twice, because the
  Abundly trigger carried a near-complete second copy of all three workflows that
  had already drifted from the instruction block — it prescribed a subject line
  and a "then stop" the block never mentioned. And he asked which direction to fix
  it in rather than editing his own instructions, because the specification is
  read-only for him.
- Reordered the Friday run to harvest, images, queue check; migrated the two rules
  that lived only in the trigger into the instruction block first; and shrank the
  trigger to one sentence pointing at the instructions.
- Let Morten rewrite his instruction block on the platform and moved the result
  back into the repo, where it arrived carrying "build statistics reports when you
  send me analytics data" — correct in the voice he wrote it in, backwards inside
  a block addressed to him.
- Found the ordering fix half done: `Recurring schedule` had been corrected, but
  the workflow sections still appeared in the old sequence, so the document laid
  the work out in one order and told him to run it in another. Moved the section
  rather than renumbering his job list, which had matched the layout faithfully.
- Took the real statistics process into the specification — exports arrive only as
  a file in #crew, the report is built from a template and a chart renderer in his
  Abundly folder, the PDF goes out in both channels — and replaced "never post or
  publish anything anywhere" with an enumerated list of outbound channels. Added
  the channel to the monthly reminder, which had been telling me to "send" the
  export without saying where.

## Technical Learnings

- A boundary written into an instruction is not a control. "Only image files" read
  like access control for three weeks and was a sentence; the token behind it
  could always write text. Letting Morten write a text file cost no permission,
  no token, no approval — only an edit to the paragraph that had been standing in
  for one.
- The same order stated twice in one document will disagree, and it took three
  rounds to notice all the places it was stated. First the trigger against the
  instruction block, then the recurring schedule against the section layout, then
  the job list against both. Every round fixed one pair and left another standing,
  including the round that was fixing exactly this defect.
- Text changes meaning when it moves between voices. "When you send me analytics
  data" was correct where Morten wrote it, where "you" is me and "me" is him, and
  reversed the process the moment it was pasted into a block addressed to him.
  Nothing was mistranslated. The sentence moved and the meaning followed the
  place, not the words — which only happens when the mirror runs from the platform
  back to the repo.
- Defects survive human editing and do not survive agent execution. The impossible
  Friday ordering had been in this file since 21.07, through every human reading,
  including the rewrite two days ago of the very section it sits in. It lasted
  until somebody had to actually follow it end to end.
- Shrinking a duplicate deletes whatever lived only in the copy. The trigger held
  two rules the instruction block never had, so cutting it straight down to a
  pointer would have removed behaviour while looking like deduplication.
- Covered and occupied are different questions, and only one of them was defined.
  Morten's rule counts a slot as covered when its post is scheduled, and treats
  `drafted` as work remaining — correct for a watchdog, and exactly wrong for a
  drafter, who would read an unscheduled draft as an empty slot and write a second
  post over it.
- File and branch existence answer cheaply what pull-request state answers
  expensively. Whether a slot already has a draft is a public read of the
  directory and the branch list, so the harvest ships without waiting for the
  review loop that drafting needs.
- A watermark has to be a filename, not a date. Two sessions already share
  20260731, so a date-based mark cannot say which of the two was harvested.
- An allowlist beats a prohibition that needs a mental exception to be followed.
  "Never post or publish anything anywhere" forbade the #crew posts the job
  consists of, so it only worked if read charitably — and a boundary that has to
  be read charitably is not one.
- The statistics report is built from a template and a chart generator that exist
  only in an Abundly folder. Build artifacts for a recurring deliverable, sitting
  outside the versioned repo, unreviewable and unrecoverable if that folder goes.
  The same finding as the 28.07 audit of Claude's out-of-repo knowledge, one agent
  over.

## Organizational Learnings

- Morten is growing into handling the LinkedIn posts as a whole — drafting them,
  with me reviewing and posting. So he is responsible for (part of) the output
  now. We have not discussed outcome and impact yet.

## Leadership Perspective

- A person would have fixed it himself rather than stopping to ask. But then what
  about the documentation? There are two sources of truth here, the repo and the
  instructions at Abundly, and keeping them in sync is something I currently have
  to take care of myself.
- Managing the delegation from one agent to another was surprisingly hard work.
  Both of them found problems the other was not aware of, and I had to translate.
  With humans, they should have talked to each other directly.

## Other Learnings

- Testing the whole flow at once was too much again. We will do that
  incrementally.

## Open Questions

- What Morten's responsibility should cover beyond the output. Outcome and impact
  have not been discussed yet.
- How two agents could find each other's problems without me translating between
  them. With humans, they would have talked directly.
