# Reviewing Morten's pull requests

The human counterpart to `MORTEN.md`. What stands there as a specification stands
here as a handgrip: which click triggers which mechanism, and which route
actually reaches him. Written 2026-09-05, against the draft pull requests #10 and
#11.

## The one channel that arrives

**A formal review with "Request changes".** The state is what counts: a comment
without one triggers nothing at all.

His specification names two endpoints for the workflow:

    /pulls?state=open
    /pulls/<number>/reviews

The second carries the review state and the review body, and inline comments on
lines live somewhere it does not name — `/pulls/<n>/comments`. **Read on 05.09
that this made them invisible to him; the first real review disproved it the same
morning.** Three comments sat on lines, the review body was empty, and he worked
all three: two done, the third refused with its reason. Line comments reach him.

What stands is the narrower rule. The body is the documented channel and the one
his specification guarantees; line comments work but rest on behaviour rather
than on the spec, so anything that must not be missed belongs in the body as
well. "Comment on this file" in the "…" menu posts to the same endpoint as a line
comment and has not been tried.

He is woken by a repository event (webhook), with the daily run as the net. When
it is urgent, add a line in **#crew**.

## Text and picture follow different rules

**Text** (`<base>.txt`): the review body is enough. Nothing but `VOICE.md` stands
behind the text, and everything else is Christian's judgement on his own voice,
which he follows. Where a request contradicts `VOICE.md` he does not follow it:
he names the wording and asks for that file to be changed first.

**Picture** (`-imageprompt.txt` / `.png`): the review body alone is not enough.
The imageprompt file is the source of truth for what an image shows, and he
checks that the correction is in it before regenerating. If it is not, he names
the wording still in the repo and generates nothing.

→ **Put the wording the brief should carry into the review.** Then he corrects
`-imageprompt.txt` in the rework and generates from it. "Make the figure
friendlier" without wording produces a question rather than a picture.

If the review moves the text, the picture is read against the **new text** —
correct the brief, regenerate, counted as *one* rework.

## When it is meant to hold in future

A review changes this one post. For everything beyond it there are two files:

- `linkedin-posts/VOICE.md` — binding for the text, read before he writes a line.
- `linkedin-posts/IMAGE-STYLE.md` — binding for the style, with a procedure of
  its own: change it there first with a dated history line, then copy the block
  into the imageprompt of the **current** post, never backwards through the
  archive.

He is instructed not to turn a change into a rule: something Christian changed
once is an observation. To make it bind, it goes into one of those two files.

**A push to main does not wake him.** His specification counts pushes, merges and
branch deletions as news; he acts on a review of his open pull request, a comment
on one, or one closed without merging. So changing the style guide is only half
the move — the other half is a second review on his pull request saying the block
is updated and asking him to copy it and regenerate. Say in it that this is the
same rework rather than a second one, or the change costs one of his two.

## Limits

- **Two reworks per post.** On a third he says in #crew that the brief and the
  result keep missing each other, and hands it back.
- **Closing a pull request is a full stop**, not feedback: he does not push to the
  branch again and opens no replacement. The mistake of 08.08.
- **Writing into his branch yourself** works, but it is expensive: a file
  Christian has touched is finished for him. It takes the draft out of his hands
  instead of sending it back.

---

# The sequence, click by click

Using a draft pull request as the example.

## 1. Open it and read the description

Tab **"Conversation"**. Morten's description is the first entry: which row he
picked and why, which beats he dropped for length, anything he could read more
than one way — and his open questions. That is the part the diff does not show.

## 2. Look at the files

Tab **"Files changed"**. In a draft pull request all four files are new, so the
diff shows the full content in green. GitHub renders the PNG directly; if it is
collapsed, use the **arrow to the left of the filename**.

To read a file without the diff frame: the **"…" menu** to the right of the
filename → **"View file"**. Each file can be ticked off with **"Viewed"** on the
right, which collapses it.

## 3. Voice check

Against `linkedin-posts/VOICE.md`. Not delegated — whether a draft sounds like
Christian is decided by Christian.

## 4. Read the picture against the finished text

Not against the brief alone.

## 5a. Requesting changes

Everything goes into one text that hangs on the whole pull request. In "Files
changed", top right: **"Submit review"** (older wording: "Review changes"; while
a review is in progress: "Finish your review" with a count). It opens a panel:

1. **The text field is the channel that arrives.** Everything that matters goes
   in here.
2. Radio button **"Request changes"** (third option, below "Comment" and
   "Approve").
3. Confirm with **"Submit review"**.

Since there is no line anchor, the text has to say where it applies:

    20260907-li-report-resources.txt
    - Paragraph 3: … instead of …
    - The closing question does not carry, because …

    20260907-li-report-resources-imageprompt.txt
    - The brief should read: "…"

Terminal equivalent, and the more reliable route while the UI keeps renaming its
buttons: `gh pr review <n> --request-changes --body-file review.md`. Check it
landed with `gh pr view <n> --json reviewDecision` — it must say
`CHANGES_REQUESTED`.

**Line comments work too**, and on 05.09 they carried a whole review on their own:
hover over the line, the **blue "+"**, then **"Start a review"** (not "Add single
comment"), and finish with "Submit review" as above. They anchor a correction to
the exact spot, which the body cannot do. What they do not do is guarantee
anything — his specification does not name the endpoint they land on — so put
what must not be missed in the body as well. One caveat learned the same day: a
comment on the imageprompt reads as being about the picture. He asked whether
"leave out Player Coach" meant the post too, rather than assuming it.

Then a line in **#crew** if the slot is close.

## 5b. Approving and merging

"Files changed" → **"Submit review"** → **"Approve"** → confirm with **"Submit
review"**.

Back in **"Conversation"**, scroll down. The merge box is green now.

1. Check that the button reads **"Merge pull request"** — not "Squash" or
   "Rebase". If it does: **small arrow to the right of the button** → **"Create a
   merge commit"**. Every pull request so far (#5–#9) was merged that way.
2. **"Merge pull request"** → **"Confirm merge"**.
3. Then **"Delete branch"**.

Terminal equivalent: `gh pr review <n> --approve`, then
`gh pr merge <n> --merge --delete-branch`.

## 6. The finish — locally

    git pull

Then work the draft over. That is the actual work; the 31.08 post went from 405
words to 350 in it. If the text moves far enough that the picture no longer fits:
correct the brief and regenerate — yourself now, because the pull request is
closed.

## 7. Set the status

In `linkedin-posts/REPERTOIRE.md`, on the post's row:

- after the finish → `approved`
- after scheduling → `scheduled (<date>)` with the filename and the post's actual
  title, which is often not the row's

Commit and push.

## 8. LinkedIn

Post and picture into the scheduler, first comment with the journal link.

## 9. Read-back

Nothing to do. Morten fetches for himself what changed after the merge — his own
duty since 30.08, not Christian's.

---

## Conflicts in REPERTOIRE.md

Two open draft pull requests both change a status cell in the same file. If the
rows sit close together, git refuses the merge although the two pieces of work
have nothing to do with each other — `IDEAS.md` #23.

So after merging the first, check the merge box on the second. On "This branch
has conflicts": **"Resolve conflicts"** in the browser, **keep both cells**,
**"Mark as resolved"** → **"Commit merge"**. Touch nothing but `REPERTOIRE.md`,
so the draft stays his.

## One ambiguity in the specification

Step 4 of the review workflow ("the correction has to be in the repository
first") is phrased generically and reads as though it covered Morten's own open
draft pull request as well — where step 11 of the drafting workflow explicitly
leaves him the file. Supplying the wording keeps the case from arising. If he
does come back with a question instead of a picture, this is where it comes from.
