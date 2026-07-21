# 20260721 - Morten's First Pull Request

## What I did

- Drafted the next two posts with Claude Code: B4 "Hiring Morten Market"
  (Mon/Tue 27./28.07) and A11 "Ich habe jemanden eingestellt" (Thu/Fri
  30./31.07) — the third instance of the pattern where one event gets told
  twice, once as an English journey report and once as a German leadership
  story. B4 was deliberately kept at the facts as they stood on 18.07, so that
  B5 keeps its own story to tell.
- Corrected a small thing everywhere: the band name is "a-ha", always
  lowercase, even at the start of a sentence. Fixed in MORTEN.md, in his
  instruction block, and in the 20260718 entry, and mirrored to Abundly the
  same day.
- Decided and specified the second expansion of Morten's role (IDEAS #18):
  **he generates the post images.** Until now, that was the last manual break
  in the drafting chain — Claude Code writes the draft and an
  `*-imageprompt.txt` into the repo, and I had to switch to another tool to
  produce the PNG, because Claude Code cannot generate images. The design:
  Morten looks for base names that have an imageprompt but no PNG, generates,
  commits to a branch `morten/images-YYYYMMDD` and opens a pull request; I
  review and merge. Three consequences I accepted knowingly — this ends his
  credential-free setup for writes, it turns #marketing from an outbound
  escalation channel into a two-way working channel, and it pulls a piece of
  IDEAS #4 (the review gate) forward onto a harmless first case: a wrong image
  costs a rejected pull request, nothing more.
- Set up the access. A fine-grained personal access token scoped to this
  repository only (Contents and Pull requests, read and write — no
  administration, no workflows), handed to Morten and validated by him.
  Branch protection on `main`: a pull request is required before merging,
  force pushes and deletions are blocked, and admins are exempt, so I keep
  committing directly from my Claude Code sessions while Morten's non-admin
  token is refused. The boundary "never writes to `main`" stopped being an
  instruction and became a control. Slack was extended so Morten can also read
  #marketing, and image generation was enabled in Abundly.
- Left the two new drafts deliberately without images, so his first job would
  be a real one. Then triggered it on demand in Slack instead of waiting for
  Friday, to watch it happen.
- Morten did the job: found exactly the two base names that needed an image,
  fetched both prompts, generated both PNGs, pushed the branch, and opened
  pull request #1 with a description listing which imageprompt each image came
  from. He did not touch the older posts that already have images, and he did
  not try to merge.
- Reviewed the two images in the Claude Code session. The first one was right
  in every detail. In the second, the robot was standing on the top step of
  the staircase, on "VERANTWORTUNG" — the exact opposite of what that post
  says, namely that only the first step is unlocked so far. Sent it back for
  rework via Slack. Morten regenerated only that one image and pushed it as a
  second commit to the existing branch, rather than opening a second pull
  request — which is better than what his instructions literally say ("a new
  branch"). Spec and instruction block were corrected to match his behaviour.
- Fixed the cause, not just the symptom: the imageprompt itself had said the
  staircase "leads from the robot upward", which is what put him on the top
  step. Reworded in the repo so the next regeneration cannot repeat it.
- Merged pull request #1 with a merge commit rather than a squash, so Morten's
  three commits stay visible in the history — in a repo whose subject is the
  collaboration itself, that record is worth more than a tidy line.

## Technical Learnings

- The review gate held on its first real use. Morten opened the pull request
  and stopped. The interesting part is that it was never tested against
  resistance — he did not try to merge, so I still do not know whether the
  branch protection or the instruction did the work. A control you have not
  seen refuse anything is a control you have to assume, not one you know.
- Style consistency survived a change of generating model. The images were
  produced by a different model than the earlier ones, and the series still
  looks like one series: same robot, same sun in the top right, same
  hand-lettered caption with the underline. What carried it was not the style
  text in the prompt alone, but the rule to fetch two existing post PNGs as
  visual references. Style is transferred better by examples than by
  description.
- A wrong image is a wrong prompt. My first instinct was to have the image
  redone; the actual defect was an ambiguous sentence in the imageprompt
  ("leads from the robot upward"). Fixing the artifact would have left the
  cause in the repository, ready to reappear on the next regeneration.
- Slack can smuggle instructions past the repository. The rework was requested
  in Slack only, so for a while the corrected image existed while the repo
  still carried the wrong prompt wording — the fix lived in a chat message.
  That is the same spec-drift class as 19.07, just in the other direction:
  then the platform ran ahead of the spec, now a conversation did. Morten's
  instructions now contain a "Reworks" rule: re-fetch the prompt first, and say
  so plainly if the repo does not contain the change being asked for.
- The agent has no identity of its own. The fine-grained token belongs to my
  account, so every commit and pull request Morten makes is authored by
  "zandercoach". In the git history, his work is indistinguishable from mine.
  Attributable commits would require a GitHub App with its own bot identity —
  which is a real question for a journey that is precisely about who did what.
- He was better than his instructions. Told to create "a new branch
  morten/images-YYYYMMDD", he reused the day's existing branch for the rework,
  because a second branch with the same name is impossible and a second pull
  request would have been noise. Good behaviour that the spec had not
  prescribed — so the spec was corrected upward to match, instead of leaving
  it as luck.
- A fine-grained token is a genuinely sharp instrument. Two permissions
  (Contents, Pull requests) on one repository are exactly enough to push a
  branch and open a pull request, and not enough to merge one, once `main` is
  protected. The boundary is expressed in the credential itself, not in trust.

## Organizational Learnings

- Giving write access was both at once — giving trust and installing a
  safeguard — and the safeguard is what made the trust cheap. I did not have
  to decide whether Morten deserved write access; I only had to make sure that
  the worst case was a rejected pull request.
- With humans, a correction that happens in conversation and never reaches the
  board is the normal price of being able to talk to each other directly. With
  Morten it isn't: we can set up a rule that he works only on the repo. The
  chat may trigger the work, but what the work is based on has to be in the
  repository.

## Leadership Perspective

- Correcting the brief instead of the worker is not something agents made
  necessary — I'd wish for more of that with people too. The second image was
  wrong because the imageprompt was ambiguous, not because Morten did his job
  badly.
- What a team needs for that is psychological safety and a culture where the
  brief is questioned first — always assume positive intent. With Morten that
  came for free: there is no ego in the room, and the prompt sits right there
  in the diff next to the result.

## Other Learnings

- The posts about hiring Morten are illustrated by Morten. B4 and A11 tell the
  story of taking him on; the images on them are his first piece of work. The
  content engine has started illustrating itself.
- The last manual break in the drafting chain closed tonight, and it happened
  almost casually — no milestone, just one tool switch that stopped being
  necessary. Draft, prompt, image, pull request: what is left for me is
  deciding and approving.
- Reviewing an image is a different skill than reviewing text. The wrong image
  was well drawn, correct in style, and contained every element the prompt
  listed — and still said the opposite of the post. No test would have caught
  that; it needed someone who knew what the post meant. That kind of review
  does not delegate.
- A history is documentation, not just plumbing. Squashing the pull request
  would have been tidier, but keeping Morten's three commits preserves who did
  what — and this is the first time that question came up, because for the
  first time someone other than me contributed commits.

## Open Questions

- Morten has no identity of his own in the repository. His token is mine, so
  his commits and pull requests are authored by "zandercoach" and cannot be
  told apart from mine. A gap worth investigating — a GitHub App with its own
  bot identity, or at least a committer identity on his commits. (→ backlog,
  IDEAS.md #19)
- Should requests and escalations live in separate channels? Since today,
  #marketing carries both — I ask Morten for work there, and he escalates an
  empty queue there. That is exactly the concern of the A12 story: an
  escalation channel keeps its signal value only as long as nothing else
  happens in it.
- Would the review gate hold against resistance? Tonight Morten opened the
  pull request and stopped, so I never found out whether the branch protection
  or his instructions did the work. A control that has never refused anything
  is one I assume, not one I know.
- Is the Abundly configuration still in sync? The spec changed twice tonight
  (branch reuse, and the rework rule that his work has to be based on the
  repo), and the instruction block over there has not been re-pasted since
  20.07. Mirroring it is the next thing to do — and the very failure mode this
  entry is about.
