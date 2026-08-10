# 20260810 - Two Hands on the Same Work

## What I did

- Morten's run opened pull request #3 on 07.08 with four images at once — for
  10.08, 13.08, 17.08 and 20.08 — and answered both questions the goal-oriented
  brief for 17.08 had asked him. He had nothing to flag as ambiguous. The idea he
  chose: both figures side by side, each wearing a name badge, the two badges
  drawn identically, "because making the two badges identical rather than making
  the robot's special is what turns it into belonging instead of promotion". He
  also named what he gave up for it — the borrowed-credential half of the story,
  because the brief had asked for one idea allowed to breathe. Two of the four
  images he had reworked on his own before delivering: the first attempts had put
  invented words on the sheets and run the caption underline into the lettering.
- Reviewed the images on 08.08 and requested changes: the human figure has arms
  and legs but no body, and all four pictures should treat the human figure the
  same way. Closed the pull request without merging shortly after.
- Wrote the correction into the shared style guide as "oval torsos" and committed
  it, then took it out again the same morning.
- Rewrote the imageprompt for 13.08 as a goal brief. The post argues that a goal
  beats a checklist, so a brief in list form would have contradicted the text it
  illustrates. IDEAS #21 was corrected with it: the first trial is no longer
  17.08 but 13.08.
- Found the PNG Morten had delivered for 10.08 carrying an invisible U+200E at
  the end of its filename. It looked correct in Explorer, but it did not match
  `<base>.png`, so the convention would have counted the image as still missing.
  Renamed it.
- Generated the images for 13.08 and 17.08 myself in ChatGPT, in parallel with
  Morten working on the same four posts on his branch.
- Reviewed the 17.08 image against its brief and found it showed five team
  members — four humans and the robot — for a team that has two. Wrote the
  headcount into the brief as a fixed constraint and regenerated.
- Found the same class of error mirrored in the next attempt: German lettering on
  the English Track B post. The brief had left the language open, so the
  generator inherited it from the German siblings. Both Track A briefs now fix
  German, the Track B brief fixes English.
- Turned the 20.08 brief into a goal brief as well, which removed the control the
  experiment had been designed with: all three briefs of that stretch are now
  goal briefs, with no checklist standing next to them in the same week.
- Checked the local repository against GitHub on 10.08 and found `main` in sync,
  but a branch `morten/images-20260807` carrying two unmerged commits and no open
  pull request.
- Read what was on it: after the "changes requested" review, Morten had
  regenerated all four images against the oval-torsos commit and written a second
  explanation for 17.08 into the pull request — this time the signature as the
  carrying idea, "the work did not change, the name under it did". He had done
  that because I told him about the review by hand; there is no structured
  procedure for it. The pull request had been closed an hour before he pushed it.
- Recorded on the closed pull request why it ended without a merge: four images
  in one commit could not be accepted or rejected individually, and the oval-torso
  correction had been written into the shared style guide, so it changed the robot
  as well, when only the human figures were meant to change. Deleted the branch.
- Made the body rule explicit in the 20.08 brief and scoped it: human figures
  always have a round head, an oval torso and limbs attached to that torso, never
  a head with limbs hanging directly off it — and the rule covers the human
  figures only, so the robot keeps his look. Starting with 20.08, not backwards
  through the archive: an older brief describes the image that was generated from
  it.
- Noticed that the sun in the top right corner had disappeared from the
  regenerated 20.08 image. It had never been a rule — it stood in every
  element-by-element prompt and therefore in every picture. Left it open for now.
- Closed the pull requests properly: all three branches deleted, no open pull
  requests, and the commits still reachable through `refs/pull/<n>/head`.
- Was not satisfied with the message of the 20.08 post any more. It sold the
  1+AI team as the same discipline as a human team, when the difference is the
  point: in a human team a flat structure runs into competing goals, and in a
  team of one human and one agent it does not.
- Chose the sharpest of three framings for the rewrite and combined it with the
  turn from another. Morten has no interests of his own, so "equal footing" is
  the wrong word here: there is exactly one will in the room, and the hierarchy
  has not disappeared, it is simply never put to the test. From there the
  contradiction has to be produced deliberately, or Morten has to be set up to
  provoke it.
- Added the condition to the ending myself: among people the contradiction comes
  for free only as long as they feel safe enough to say it out loud.
- Rewrote the imageprompt for the new message and moved the caption from
  "Mittendrin" to "Kein Widerspruch". The new image has the human ask "Wie siehst
  du das?" and Morten answer "Ich habe keine eigenen Interessen."
- Updated the A19 row in `REPERTOIRE.md`: working title, leadership translation,
  and the note calling its brief the deliberate checklist control, which no
  longer exists.

## Technical Learnings

- A closed pull request swallows the agent's reaction. Morten did react to the
  review — he regenerated all four images and wrote why — but only because he was
  told about it by hand, and by then the request was closed, so the work landed on
  a branch nobody opens. He can act on a review once he knows of it. What is
  missing is any structured way for him to find out that one happened, and that
  the request is closed.
- Four images in one pull request cannot be reviewed. Accepting or rejecting is
  all-or-nothing, so a single objection kills three pictures that were fine. The
  batch size of a delivery decides whether a review can be granular at all.
- A correction written into shared boilerplate changes everything the boilerplate
  touches. "Oval torsos" was aimed at the human figures and reached the robot
  through the same paragraph. A correction needs its scope stated, not only its
  content.
- Reverting a shared rule after an agent has generated against it strands his
  work. Morten's rework follows a style guide that `main` no longer carries.
- An invisible character passes every human check. The U+200E at the end of the
  PNG filename looked right in the file browser and broke the `<base>.png`
  convention, which would have made the image count as missing forever.
- Reviewing an image against its brief catches what looking at the image does
  not. Two errors of the same class came through: four colleagues who do not
  exist, and German lettering on an English post. Both were well drawn, in the
  right style, and said something untrue.
- Changing the form of a brief loses what the old form carried implicitly. The
  sun was never a rule; it survived because every checklist repeated it. The goal
  brief does not mention it, and it vanished without anyone deciding so.
- A change of message travels further than the text it is written in. The old
  claim of the 20.08 post sat in five places at once: the draft, the imageprompt,
  the caption, the picture and the repertoire row. Changing the post and stopping
  there would have left the image arguing against the text it illustrates — the
  same failure as on 21.07, only self-inflicted from the other end.
- The read-out of the experiment did arrive. Morten answered both questions in
  the pull request body, twice — it was believed lost only because it lived in a
  place that was already closed.

## Organizational Learnings

- Working with Claude and with Morten on the same four images was both at once:
  two strands open at the same time, and two strands that knew nothing of each
  other. In future one strand should work towards a goal — in this case "produce
  a fitting LinkedIn post, text and image".

## Leadership Perspective

- Closing the pull request was neither a shortcut nor a lack of trust in the
  agent's ability to rework it: I had lost the overview and wanted to start
  again.
- Morten finding out about a review and Morten contradicting me are not the same
  thing. A review he would simply work through. Contradiction I would have to ask
  for.

## Other Learnings

- Generating the images myself again comes out of two things at once: the flow is
  not good yet, and I tested too much in one go. Smaller tests help — in this
  case one image for one post, not four images for four posts in a single pull
  request. Then I could have tried the changes to the image prompt out directly.
  With Morten too, if he had been able to react to pull requests.

## Open Questions

- How the flow has to look so that Morten can take over the whole post.
- How you ask an agent for contradiction.
