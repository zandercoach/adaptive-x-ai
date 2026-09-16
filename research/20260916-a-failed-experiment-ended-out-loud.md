# 20260916 - A Failed Experiment, Ended Out Loud

## What I did

**Reviewed Morten's harvest, pull request #12.** Sixteen A rows and four B rows
from the four entries after the watermark. Four points went back: A64, where the
leadership translation carried a consequence I never drew — the one failure this
job can produce that reads perfectly well in review; a rule count that said four
in one row and five in another; a sentence lifted from `Craft`, which is a record
rather than my voice; and a row citing one source while using two. He reworked
all four in three minutes.

**He found a third instance of the number and did not act on it.** A51 still said
"five new rules", outside the two rows I had named. He reported it, left it
alone, and said that leaving it meant the rows now disagreed. On 04.09 the same
diligence had been a break-out from his ruleset; this time it was the version
that row itself recommends.

**Consolidated the queue from twenty-four open A rows to five**, and B from nine
to five. Three small merges, four drops, sixteen rows parked as bullets. Merges
were kept to one source each on purpose: A20 and A24, the two four-source rows,
are the ones that had to be retired on 31.08.

**Then the consolidation turned out to have parked a row with a live post behind
it.** A26 read `idea` on main, because Morten writes the status only on his own
branch — the occupied signal was the draft on the open branch, which is exactly
what *occupied* covers, and the run did not look there. Pull request #13 had been
open since 14.09, and we knew it was. Restored byte-identical so it merged
without conflict.

**Christian rejected that draft outright and dropped the row.** Not because the
slot had slipped — the post could still have gone out today — but because A26
promises more than its scene carries, and something else mattered more. The
pull request was closed with the reason in a comment first, the branch
deleted, and with it the last signal pointing at the week.

**A replacement went out the same afternoon.** An on-demand request in #crew named
B19 — a Track B row written in the Track A form, which the one-track rules allow —
with one beat only and the lesson supplied in Christian's own words. Draft,
review, finish and scheduling inside a few hours, for Thursday morning rather
than the Tuesday or Wednesday the cadence names.

**Shortened `REPERTOIRE.md` by 4.5k characters** with four cuts that lose nothing,
after measuring where the length actually sits.

## Craft

- **A status cell is not the whole truth about a slot.** The occupied signal can
  live on a branch, in an open pull request, in a file that never reaches main.
  A pass that reads only the table will delete work that exists. The check that
  was missing is a cheap one: list the open pull requests before removing rows,
  especially when you already know one is open.

- **Parking is not the gentler form of dropping.** A dropped row keeps its text
  in the table; a parked row leaves and becomes a bullet. So parking A45 turned
  A47, the row that had been merged into it, into the last full text of that
  argument in the file — a consequence nobody chose.

- **Measure before promising to shorten.** Of 72k characters, only 4.5k came out
  without a decision: two paragraphs whose record lives in `MORTEN.md`, a closed
  experiment whose result lives in `VOICE.md`, an enumeration the status cells
  already carry, and three merged rows that are genuine duplicates. Everything
  beyond that is content, and cutting it is an editorial call rather than a
  cleanup.

- **Inference has a shape you can check for.** In every harvested row the quoted
  reflection came first and one generalising sentence followed. Where that
  sentence restated what Christian drew, it earned its place; in A64 his
  reflection was one line and the generalisation was the whole lesson. The tell
  is the ratio, not the wording.

## Business Model

- There is no learning journey without failures, so hiding one would make the
  journey dishonest. The failed experiment does not damage the brand, it adds
  to it.

## Leadership Model

- Morten reporting the third instance of the number and not acting on it was
  both at once: an agent following a rule he did not have before, and my trust
  growing. It still has to confirm itself.
- Neither of the day's two setbacks was a mistake of Morten's. He wrote a
  sensible post; what was missed — by Claude, where the commit to main is
  concerned — was that a merge conflict was coming, although we knew a pull
  request was still open. And the draft was not lost to that: I discarded it
  actively, because something else mattered more to me, and it could still have
  gone out today.

## Operating Model

- In a real team I would propagate pair programming and working directly on
  main. Morten is asynchronous on purpose, because that is what there is to
  learn from, so what it takes instead is the discipline not to leave pull
  requests open as long as this one was.
- Harvesting insights into the repertoire and drafting LinkedIn posts should be
  pulled apart rather than run one after the other.
- And Morten should work his harvest findings into the existing rows instead of
  appending them, describing every change he makes in the pull request comment.
