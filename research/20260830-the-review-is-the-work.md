# 20260830 - The Review Is the Work

## What I did

- Reviewed and merged Morten's harvest, pull request #6: ten rows out of the
  20260824 entry, A35-A44 on Track A and B15, B16 on Track B, with the watermark
  moved to the entry he had just read.
- Corrected A41 on main afterwards. The row had kept Article 50's exemption and
  dropped the condition it hangs on — that the duty applies to content meant to
  inform the public on matters of public interest, and only then does human
  review discharge it. Harmless in a queue row, not harmless in the post that row
  is for.
- Reviewed **his first text draft**, pull request #7: B8, the company-brain
  report for Mon 31.08. One rework, done by him — vary the closing disclosure,
  name Claude on first mention — then merged. Then finished it myself across four
  commits: *accountable* back into the closing line, the admission that a memory
  is what we built, the name that can lose a discipline, and the trim.
- Made the two numbers in `VOICE.md` limits again. 250-350 words is a limit, not
  a description: the reports of 10./24./31.08 ran 398, 399 and 398 and I read all
  three as too long, my own drafting included. And the em-dash row said "once or
  twice per post", which reads as a floor; it now says at most two, fewer better,
  none fine. B8 came down to 350 by dropping beats, not by squeezing sentences.
- Merged pull request #8, the image for B8, and approved the post with text and
  picture both in.
- Built the rework path the drafting stage had been built without — step 11. The
  workflow had nine steps and nowhere for a review to land, the review workflow
  pointed at a "Reworks" section that is about images from its first sentence,
  and the hard boundary forbade editing an existing draft at all. The distinction
  that resolves it: a draft is Morten's while his pull request is open and mine
  from the merge on. Fixed in five places at once.
- Built step 12, the read-back. A merged pull request swallows the reaction
  exactly as a closed one did on 10.08 — four commits carried tonight's finish
  and he would have seen none of them. Not a notification and not a duty on me:
  before writing, he fetches his own last merged draft at its head SHA and on
  main, reads the commit messages between them, and reports in his next pull
  request what changed and what he takes from it.
- Made three expansions after saying the collaboration felt hakelig: the picture
  rides along inside the drafting pull request, one status edge (`idea` →
  `drafted`) moves to him, and the review loop becomes event-driven on an Abundly
  webhook with the daily run left behind it as the net.
- Cut the instruction block by a third, 5188 words to 3540, with no rule dropped
  — checked by walking every prohibition, file, count and URL from the old block
  into the new one. What went was the history of why a rule reads as it does,
  which belongs above the fence and is already there.
- Called **stage 3 four days early**, both tracks instead of the Track B slot
  only, because the first draft had held up. Pull request #9: A43 for Thu 03.09,
  the first German post an agent has drafted, read against A22 and A31 rather
  than against the English reports.
- Fixed the two files his German draft had named rather than worked around:
  `VOICE.md` and `REPERTOIRE.md` still dated stage 3 to 04.09, six hours after
  MORTEN.md had moved. Gave a home to two rules that had none — what a status
  cell carries at `drafted` against from `scheduled` on, and that the image
  brief's "the two figures of the series" does not mean both must always appear.
- Reworked A43's German myself, and scheduled it. Both slots of the week now sit
  in LinkedIn's own scheduler; next open slot is Mon 07.09.
- Brought Abundly into line in one pass: the shortened block replacing the old
  one whole, the webhook trigger, the daily review run. The trigger carries one
  sentence and not the event list, which stays in the repo.

## Technical Learnings

- A stage can be complete and still have no path for what happens after it
  succeeds. Drafting was built with nine steps, all of them about producing a
  draft, and the first review had nowhere to land. Nothing made the gap visible
  until a draft existed — the same shape as 24.08, where a complete list of
  prerequisites was missing the job itself.
- The finish is where the post changed, and it was invisible to the one who wrote
  the draft. Four commits took B8 from 405 words to 350, gave the title a
  question, added a claim, removed a maxim and put it back. "Morten drafts, I
  finish" is the whole design, and the finish reached nobody until step 12
  existed.
- A merged pull request swallows feedback exactly as a closed one does. The 24.08
  loop fixed the closed case only, because a merge reads like agreement.
- A target reads as a floor when it should be a ceiling. "Once or twice per post"
  had three drafts in a row put a dash in for the density and take it out again
  on the voice check.
- A status transition can only belong to whoever can observe it. `idea → drafted`
  is Morten's own fact; `approved` is my judgement, `scheduled` is my action in
  LinkedIn, `posted` is a fact he is forbidden to go and look up. Giving somebody
  a status they cannot observe makes them guess.
- A capability is not a permission, and a permission is not a control. The 12.08
  finding was a sentence mistaken for a control; today the mirror-image error
  went into the spec and came out again against the token's actual scopes.
  Writing to main and merging are held by branch protection and the code-owner
  review; closing a pull request is held by a sentence alone.
- The same defect a third and fourth time: a rule changed in one place and left
  standing in the others. It happened six hours after writing the rule against
  it, and Morten was the one who found it.
- An event's meaning belongs where the work is, not where the trigger is. The
  webhook says one sentence — on an event here, run the review workflow — and
  which events matter stays in the repo beside the workflow. Two copies of that
  list would be the 12.08 defect rebuilt on purpose.
- History inside an instruction block is weight without effect. It is pasted into
  Abundly and read on every run; the reason a rule has its current wording is for
  the reader of the file, not for the agent executing it.

## Organizational Learnings

- What felt hakelig about the collaboration was that the working steps are still
  very small-grained, with hand-offs for quality control and for making sure that
  Morten does the right things right.
- I also have to become more confident with pull requests in git — I still have
  to learn how collaboration over git really works well.
- And Slack as a communication channel is an indirection compared to prompting
  directly. When Morten reacts to a message is still open: whether I have to
  address him with an @ or whether he reads along in a thread by himself is
  something I would have to find out.
- The handover has so far only moved the work rather than taken it away, because
  the review process is the actual work. And it made it harder, because I now get
  to work with pull requests, which I am still unsure with. The second part will
  get better and faster; the first will stay.
- What I gain is that I start from a synchronised state: a draft with its picture
  and its `REPERTOIRE.md` row already noted, so I do not have to produce that
  state myself. And I learn along the way how agents are usefully used and led.
- What it costs me is more tokens, because an agent hosted on a commercial
  platform like Abundly is more expensive — the tokens Morten spends there, for
  his own work and for talking to me, also pay for the infrastructure. And it
  takes longer.

## Leadership Perspective

- The draft's result was good, but the driver for pulling stage 3 forward was the
  fragmentation of the process, with many hand-offs and many sources of error.
  Since it makes no difference apart from a few tokens whether I check every
  intermediate step or only the result, the time saved on my side mattered more to
  me than controlling Morten in small pieces.
- A no to the result restarts the whole run, or only the parts that are not right.
  But reworking goes so fast that I can run more iterations.
- Building the read-back as Morten's own duty rather than as feedback I owe him
  lies in the matter itself: he can fetch it at any time and simply does it if he
  needs it. Before people fetch feedback for themselves it takes a few emotional
  factors, above all the psychological safety that the relationship is a
  constructive, supportive one and that the feedback will help move their personal
  development forward.
- In German I am the measure, but in English too I have noticed that many AI
  formulations still give away where they come from. I want to bring my own way of
  writing and my own tonality in more strongly here, to tell my story in my own
  language. Too much AI puts the potential readership off — and I may already have
  that problem, because the impressions and interactions on my posts are sinking
  slowly but steadily.

## Other Learnings

- The finding that cutting the instruction block by a third cost no rule is not
  about the block. It holds for everything Claude writes for me, commit messages
  included: it may gladly be shorter, more concise and more to the point.

## Open Questions

- How I become confident with pull requests, and how collaboration over git really
  works well.
- Whether the impressions and interactions on my posts are sinking because the
  texts still sound like AI.
