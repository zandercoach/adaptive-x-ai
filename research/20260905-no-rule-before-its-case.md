# 20260905 - No Rule Before Its Case

## What I did

**The 04.09 entry was finished and renamed.** Six reflection questions were
answered in an interview, one at a time. The working title *A figure without its
window* named the day's retraction — a June figure that two exports put at 726
and 762, correct on both sides, and read as a contradiction only because no
report carried its window. Christian's call was that the title should carry the
decision instead: *The numbers retired a track*. The README index turned out to
be two entries behind, so 30.08 and 31.08 were linked in the same pass.

**The language rule got wider.** On 02.09 it hung on execution: binding
instructions in English because agents run them, everything else German. That
boundary left every document written for a human to be argued one at a time — and
`REVIEW.md`, written this morning in German for exactly that reason, was the
first argument. **Decided 05.09: every new document is English**, process and
reference documents included, whoever reads it. German is now a request Christian
makes, or an audience that speaks it — posts, website, decks, handouts, offers,
client material.

**And English became British English.** The trigger was a question of Morten's
that nothing in the repo could settle: he had written *characterise*, the queue
row said *characterize*. The repo held 46 occurrences of "organization" against
nine of the hashtag `#AdaptiveOrganisations` — a contradiction sitting on the one
word that says where this business stands. Oxford spelling was the comfortable
way out and does not work: it writes *organize* and would collide with the
Society's own name inside the same sentence. So `-ise`, with the exceptions
carrying the weight — nothing machine-readable, no quotations, no proper names,
no established terms (`characterization test`), and no structural names already
in use, such as the journal's `Organizational Learnings` heading. Nothing was
converted backwards except `docs/`, which only ever describes the current state,
and `RESOURCES.md` alongside it, because the two carry the same sentences.

**`REVIEW.md` was written, as the human counterpart to `MORTEN.md`.** That file
says what Morten does with a review; nothing said what makes a review reach him,
or which click produces which mechanism. It went in next to the specification it
mirrors — the channel, the difference between correcting a text and correcting a
picture, where a rule has to go to hold in future, the limits, and the click path
through GitHub.

**The block did not say it, so nothing was generated.** Christian's review of
pull request #10 asked for three things, two of them on the picture: leave out
"Player Coach", show the company brain as documents and decisions, and draw
one-line arms with round hands and feet. Morten did the first two and refused the
third: `IMAGE-STYLE.md` says "thin arms and legs attached to that torso" and
nothing about one line or two, and a correction living in a review comment
reaches the next image from nowhere. He asked for the file to be changed first,
with a dated history line. He also held the PNG back — the brief had moved and
the style rule was about to, so one regeneration covering both was worth more
than two, and he counted it as the same rework. Nothing in his specification says
that; he worked it out.

**The rule went into the source, and then nothing happened.** The style block now
says single-line arms and legs, each ending in a small round hand or foot, human
figures only, in force from the 07.09 post onward. It was committed and pushed —
and Morten did not stir, because pushes to main are *news* to him and not a
trigger. It took a second review saying "the block is updated, copy it and
regenerate, this is the same rework" to move it. He then replaced the block
verbatim, regenerated, and noted that the two reference PNGs still show the old
limbs, which is correct.

**Pull request #10 merged and scheduled** for Mon 07.09 as *What the company
brain reads*.

**Pull request #11 produced the first draft to be thrown away whole.** Morten had
drafted A21, whose scene — the goal-shaped image brief of 06.08 — B13 had already
told in English on 24.08. He named the risk himself in the pull request
description and offered A25 or A26 as alternates. Both fail the same test: A25's
honest-asymmetry half went out in B8 on 31.08, A26's second half is B13 again.
The replacement was **A28 "Wer darf die Regeln schreiben?"**, the topmost open
row whose material is genuinely unwritten. He renamed the three files, put A21
back to `idea`, set A28 to `drafted`, and drafted against the new style block.
Merged and scheduled for Thu 10.09 as *Dreimal hat es funktioniert. Machen wir
eine Regel daraus?*

**The queue was cut from thirteen open A rows to nine, and nothing was deleted.**
Two new statuses carry it: `dropped (date, reason)` for a row that will not be
written, `merged (date, into <row>)` for one whose material moved elsewhere. The
31.08 pass had moved five rows to *Parked*, which shrinks a row to a bullet; this
one leaves the text where it is and puts the decision in the cell. A21 and A25
were dropped for scenes already published, A48 for being far too thin, A47 merged
into A45 — which now carries both halves of the review argument, that reviewing
is the work and where to put it. A25's disclosure beat was split out as a new row
A50 rather than falling with it. A26 lost the half B13 had told, and its manager
line was rewritten: the coordinating role loses its reason to exist as a
cross-functional team earns responsibility and autonomy for itself, which AI will
drive further — not as the unit shrinks toward "1 + AI".

**Track B stopped going out; it did not stop existing.** Two places read
otherwise, and one of them sat in the block Morten reads every run: the drafting
workflow called Track B "a track that no longer runs", a few lines from the
harvest that still proposes B rows every Friday. One track is an experiment
rather than a verdict, the journey material may yet be played out on a channel of
its own with Substack among the candidates, so both files now say the harvest
keeps feeding both.

**A finding of my own did not survive the first real run.** `REVIEW.md` said
inline comments on lines never reach Morten, derived from his specification
naming `/pulls/<n>/reviews` and not `/pulls/<n>/comments`. Christian's first
review put three comments on lines and left the body empty, and Morten worked all
three. The file now carries the narrower rule instead: the body is the channel
his specification guarantees, line comments rest on observed behaviour, so
anything that must not be missed goes in both.

Twenty-two commits in `adaptive-x-ai`, six of them Morten's, one in the workspace
repo. Mirror refreshed twice.

## Technical Learnings

- **A correction that is not in the source file is not a correction.** The style
  block said "thin arms and legs" and left the ends open, so a review asking for
  round hands asked for something the source did not say. Morten generated
  nothing and asked for the file first. That rule was written on 10.08 after
  "oval torsos" in the shared header silently reached the robot as well; today
  was the first time it held rather than failed.

- **A finding derived from a specification is a hypothesis until something runs.**
  The specification names one endpoint, so I concluded the other one was
  invisible to him and wrote it into an instruction file as fact. Three line
  comments and an empty review body disproved it hours later. What survives is
  the narrower claim — the body is guaranteed, the line comments are observed —
  and the difference between those two words is the whole lesson.

- **A push is not a notification.** The corrected style block sat on main,
  committed and pushed, and nothing happened: pushes, merges and branch deletions
  are news to him, and only a review, a comment on his pull request, or a closed
  one is a trigger. Half of "change the style guide" is changing the file; the
  other half is telling the agent that it changed.

- **Two corrections, one regeneration.** Morten held back the PNG because the
  brief had moved and the style rule was about to, and counted both as a single
  rework. The cap of two exists to stop a brief and a result from missing each
  other repeatedly; spending one of them on an image that was going to be redrawn
  anyway would have been the letter of the rule against its point.

- **`-ize` is British, and still wrong here.** Oxford spelling — OED, Oxford
  University Press, much of the UN and ISO — writes *organize* and is British
  English. It was the comfortable compromise for a hand trained on American
  spelling, and it fails on the one word that matters: the Society writes
  *Organisations*. A house style has to survive contact with the names it uses.

- **Deleting a row and ending a row are different operations.** The queue only
  knew the move to *Parked*, which compresses a row to a bullet and leaves the
  reasoning in a second place. Two statuses replace it, and it had to be two:
  calling a merged row "dropped" makes the column say the opposite of its own
  parenthesis, and a column you have to read against its explanation is not doing
  its job.

- **The rows that fall are the ones whose scene was already published.** Three of
  the four drops today, and the discarded draft as well, came down to the same
  test: has this scene gone out already, in either language? It is a cheaper test
  than judging a row's quality, it can be answered from the queue alone, and it
  is the one Morten cannot apply for himself, because a published post's scene is
  not a fact his instructions let him look up.

## Organizational Learnings

- Morten picks the subject of a draft himself, by the order of the repertoire.
  His assessment of how current and how effective a row is, paired with
  alternatives, is genuinely useful framing — it turns the draft into a
  recommendation about content rather than a pure piece of execution.

- A dropped row stays visible as a decision, where a deleted one would be a loss.
  But it is also a safety net born of the fear of losing things — the same one
  that stops companies deleting anything in their backlog. Maybe I should bring
  myself to do it after all.

## Leadership Perspective

- Morten refusing the instruction and asking for the file to be changed first was
  diligence, not obstruction. That is exactly how he should work.

- I rely on what Claude tells me about how something behaves, and verify by spot
  check.

## Other Learnings

- Rules should come about the way both of today's did: out of the concrete case.
  Abstract rules written in advance do not work.

## Open Questions

- Nothing is left open after this day.
