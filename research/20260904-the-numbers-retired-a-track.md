# 20260904 - The Numbers Retired a Track

## What I did

**The August LinkedIn report arrived, and the finding in it did not survive.**
Morten reported 1.968 impressions for August against 2.202 in July, with the
reading that Track A carried the month: four German leadership posts at 285
impressions on average against six English journey reports at 94. Ten posts had
bought less reach than seven the month before.

Reading that against July was impossible, because no report had ever broken a
month down by track. The July report gave one average for seven posts. So the
first move was a question back to Morten: the per-post table for both months,
single values rather than averages, from one data pull — plus the three
inconsistencies that had turned up while comparing the two reports (July at 54
engagements in one and 53 in the other, ten August posts against nine in the
repo, and a June figure that two derivations put at 762 and 821).

**He answered with the raw table, and corrected himself twice unprompted.** The
18.08 post in his August figures has nothing to do with the journey — the only
row of the period whose slug is text rather than hashtags, which is how it got
counted as Track B. He also flagged two things nobody had asked about: that the
daily sheet and the per-post sums are different measures, and that all figures
are cumulative to the export date, so the newest posts are systematically
undercounted against the older ones.

**I then accused him of fabricating a reconciliation, and was wrong.** He gave
June as 726 where the export I was reading said 762, wrapped in the line *"726 +
2.202 + 1.968 + 95 = 4.991, geht exakt auf"*. I called it a digit swap in a
figure his own July report had had right, and a check built from numbers made to
fit. Christian named what I had overlooked: two exports, one starting 7.6. and
one starting 1.6. The first six days of June carry 36 impressions, and Morten had
written his window down — "7.6.–30.6., Tagesblatt". Both figures are correct.
The retraction went into the archive and into a commit of its own.

**The figures, read per track for the first time, ended the two-track model.**
Track A: 621, 200, 426, 290, 313, 372, 166 — a band around 290 with a premiere
above it. Remove the premiere and July's 313 against August's 285 is −9 %, which
is noise. Track B: 524, 257 · 532, 180, 157, 224 · 137, 138, 71, 55, 64 — a
monotone fall to a floor near 60, −50 % across the same cut even with its own
opener removed. And Track B carried the *higher* engagement rate in both months,
3,0 % against 1,5 % in July and 2,8 % against 2,3 % in August: not rejected, not
shown. The season does not explain it, because then both would fall. The two
tracks were never two contents — A23 is a journey episode told as a leadership
story and took 290 in the week its Track B twin took 137.

Decided: **one German track from the week of 14.09**, one post a week Tuesday or
Wednesday, journey material in leadership form, the freed second slot spent
commenting under other people's posts rather than on a second broadcast. The week
of 07.09 runs two tracks unchanged so the switch does not overlay stage 3 of the
handover.

**The numbers got a home.** Three monthly reports had lived in a Slack thread and
nowhere else, and two figures from the July report could not be recomputed because
that export had been thrown away. They are now in `brand/reach/`, private —
reach and follower growth are business data during a repositioning, and one repo
is one confidentiality boundary. The findings stay public as prose in this
journal; only the figures are private. Three layers per export: the raw xlsx as
the source, a markdown table as the readable rendering, the PDF as the delivery.
Christian renamed the files afterwards, and the pattern was written down as a
convention local to that folder: `<date>-<channel>-<kind>`, all lowercase, the
date's granularity following the artefact's period.

**Morten's statistics job gained five rules and a second artefact.** The
population comes from the repo and not from the export's hashtags; per-post sums
for track comparisons and the daily sheet for month totals, named as such; the
window a figure covers; the comparison month recomputed from the current export
rather than quoted from the earlier report. And every report now ships as the PDF
*and* as a per-post table, both named — `YYYYMM-linkedin-report.pdf` and
`YYYYMMDD-linkedin-export.md`, carrying different dates on purpose.

**Three of those rules had landed where he would never read them.** MORTEN.md
splits into a half that talks *about* Morten and a fenced block that talks *to*
him; only the block is extracted by spec-sync into the document he reads each run.
The rules went into the prose half. I found it while looking for where the fourth
one belonged; Morten found it independently, said so, and followed them anyway
that same day — because they stood in the repo and were unambiguously addressed
to him — while naming that they would not reach him next run.

**And his first application of the population rule broke it.** The rule hung the
population on `REPERTOIRE.md`; the queue begins on 13.07, so the three posts
before it carry no row, June came out with no journey posts at all and July lost
its strongest report. He reported it rather than absorbing it. The population now
hangs on the draft file in `linkedin-posts/`, whose first line names its track.

**The one-track switch was carried through four files** — the cadence rules, the
drafting workflow and the queue check in `MORTEN.md`, the cadence paragraph in
`REPERTOIRE.md`, the revision in `IDEAS.md` #1, and Part 2 of `VOICE.md`. The
last of those needed six decisions that were Christian's alone, asked one at a
time: the journey anchor stays mandatory and the subject stays the journey, for
now; *full disclosure, not a how-to* migrates out of the retired report format
into the story and limits the translation, so the lesson is told rather than
recommended; length becomes 200–300 words; a post now has a defined ending —
question, anchor, disclosure, hashtags, in that order — and the "Next up" teaser
dies with its series; the hashtag block is a constant core plus a tag naming this
post's subject.

**The first-comment experiment was closed and read out.** The in-body pointer came
out of both tracks from 10./13.08. Measured on the stable track — Track B being
useless as an instrument, since it was already falling before the cut — the
stories with the pointer averaged 305 impressions and those without 284. Minus
seven percent against a per-post spread of 166 to 426 is noise. It costs nothing;
the number is written down next to the rule so it is not run again.

**Pull request #10 was conflicting**, and the conflict was nobody's doing: Morten
flipped B9's status cell to `drafted` at 08:08, the queue was edited three times
over the day, one of those putting B8 on `posted`, and B8 and B9 are neighbouring
table rows. Resolved by merging main into his branch and keeping both cells,
touching nothing but `REPERTOIRE.md` so the draft stays his to rework. Filed as
`IDEAS.md` #23.

Eleven commits in `adaptive-x-ai`, five in `brand`, one in the workspace repo.
Mirror refreshed twice.

## Technical Learnings

- **A monthly average hides the thing that decides.** Three reports had been
  produced before anyone read a month by track, and the moment it was read the
  conclusion inverted twice: first from "reach is falling" to "one track is
  falling", then from "Track A is the bigger loser" to "Track A is flat and the
  apparent decline is a premiere leaving the average". Neither move needed new
  data. Both needed the data cut differently.

- **A figure without its window is not a figure.** 726 and 762 are the same June.
  Two exports with different start dates, a difference of 36 impressions across
  six days, and no report saying which window it stood on. That turned two correct
  numbers into an apparent contradiction and produced an accusation that had to be
  withdrawn. The same class as the daily-sheet-against-post-sums confusion Morten
  had flagged himself, one dimension over.

- **Keeping the raw file is what makes a claim checkable a month later.** The July
  report's 54 engagements cannot be recomputed, because that export is gone.
  Everything else that was in question today was settled by reading the xlsx —
  the June window, the since-launch total, the per-post values, the hashtag
  pattern, the word counts. Where the source was available the question closed in
  minutes; where it was not, it stayed open permanently.

- **An outlier at the start of a series poisons every average that includes it.**
  Track A's premiere at 621 and Track B's opener at 532 both sit in July and in no
  later month, which alone accounts for most of the month-over-month fall. The
  same correction applied to both tracks and moved them in opposite directions: A
  from −32 % to −9 %, B from −66 % to −50 %.

- **A rule is only in force where it is executed.** `MORTEN.md` deliberately
  separates the half that explains from the block that instructs, and only the
  block is synced into what the agent reads. Writing a rule into the explaining
  half is indistinguishable from writing it — same file, same commit, same review —
  until the run where it does not apply. The mechanism was working correctly the
  whole time and reported "unchanged"; what was wrong was the placement.

- **Two of my own recommendations did not survive contact with the data.** "No
  repeated hashtag signature" was written from a guess; the track that works
  repeats a signature of three tags in eight posts out of eight, and what the
  dying track lacked was the varying tag that said what the post was about. And
  the length rule I would have tightened turned out never to have been met: the
  stated floor of 120 words was not approached once in eight posts.

- **Case-only renames do not reach the index on Windows.** `core.ignorecase` is
  true, so renaming three PDFs to lowercase left `git status` silent while the
  repo kept the old spelling — it would have come back on the next case-sensitive
  checkout. `git mv --force` per file is the fix. The same silent-drift class as
  `core.autocrlf`, one attribute over.

- **A merge conflict can be a property of the storage rather than of the work.**
  B8 and B9 have nothing to do with each other; they are neighbouring rows in one
  markdown table, and that is enough for git to refuse. No amount of coordination
  between the two writers prevents it — only a different shape for the data would.

## Organizational Learnings

- Morten contradicting his own report, following a rule he could see would not
  reach him, and reporting that the new population rule excluded three posts that
  plainly belong to the journey did not change the briefing — it changed the size
  of the next handover. I gave him more yesterday, and the frame for the LinkedIn
  posts changed on the basis of the impressions and engagement feedback. That may
  first be allowed to work again, then we look further. Step by step.

- Running the whole day as the interface was both at once — a bottleneck and the
  thing that makes the arrangement work. As a human I become the bottleneck when
  the output of one or several agents keeps rising. That makes a different,
  goal-oriented process necessary, one in which agents decide more themselves in
  order to reach a goal. But that needs the right conditions — the harness — so
  nothing unforeseen happens. On the other hand I remain responsible both for the
  steps chosen and for the result. That balance may be found individually in
  every context.

## Leadership Perspective

- Accusing Morten of manufacturing a reconciliation cost us nothing here. In other
  contexts wrong decisions of that kind can have serious consequences. Again the
  question of the fitting harness.

- Morten works very well on the basis of his instructions. That he reacted to a
  change in his *description* — outside the instructions — is a double-edged
  sword. It was a break-out from the ruleset, well meant and sensible, but still a
  break-out. I would have found it more sensible if he shared his finding but did
  *not* act on the basis of changes outside his instructions.

## Other Learnings

- The two rules of mine that had to be narrowed — "no repeated hashtag signature",
  which the data contradicted, and "never edited afterwards", which would have kept
  a dead file reference alive — are the normal price for rules written quickly.

- Evaluating the LinkedIn posts becomes much easier through the automation of the
  report and the support in interpreting it from Morten and Claude. Defining and
  running experiments in that context becomes easier too.

## Open Questions

- How I can hand Morten more work goals in future without letting the
  responsibility for them slip.

