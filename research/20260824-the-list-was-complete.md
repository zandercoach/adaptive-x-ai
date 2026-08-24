# 20260824 - The List Was Complete

## What I did

- Found both slots of the week empty, Mon 24.08 and Thu 27.08 — and found that
  the Monday report had not been mine to write. Stage 2 of the handover had
  Morten drafting it on Fri 21.08. No draft and no pull request arrived, and none
  of the three prerequisites the stage was gated on had been built.
- Picked the week's pair from the queue rather than from chronology: B13 for
  Monday and A31 for Thursday, over the in-order candidate B8, whose pair A25
  would have repeated A19 of 20.08 one week later. A31 instead continues where
  A19 ended, on the contradiction that has to be asked for.
- Resumed the first comment, dropped since 06.08 because I was away, and kept the
  in-body pointer out so the experiment keeps one defined variable. It is read out
  from the monthly export at the end of August.
- Wrote both posts. Renamed the report from "Two hands" to "Four hands on the same
  work", two per person, because two hands read as ambiguous.
- Cut the paragraph carrying the parallel work out of the report, then put one
  sentence of it back. Without it the title had no story left and the argument had
  moved onto A31's ground, so the pair told the same thing twice instead of
  dividing it.
- Decided that every post says it was made together with AI and that I reviewed
  it, and that the word for what stays with me is *accountable* rather than
  *responsible*. Put it into `VOICE.md` as a rule, dated and marked as not coming
  from the voice interview.
- Asked Morten in #crew for both images. He delivered them in pull request #5,
  named the idea behind each and what he gave up for it, and asked one question:
  whether the caption underline has to be black or may be a colour accent. He
  decided for black and said why.
- Checked both images against their briefs before merging — figure count, the
  language of the lettering, the exact caption text, and the filenames byte for
  byte. Merged as a merge commit so his two commits stay his, and deleted the
  branch.
- Answered his question in the pull request, and put the answer where it lasts:
  black is the rule, and it went into the style guide rather than staying in a
  review comment.
- Built the three things the drafting stage was gated on. A review workflow that
  starts every run by listing his own open pull requests and their reviews, with
  three rules attached: a pull request closed without merging is a full stop, a
  correction living only in a review comment gets named rather than followed, and
  reworks are capped at two per post. *Covered* and *occupied* split into two
  words. And one pull request per post in the image job, replacing one per day.
- Found while building that the list of prerequisites was complete and the job
  itself was missing: there is no drafting workflow. The design had been written
  in prose on 12.08 and never turned into an instruction. Wrote it as job 3,
  scoped to the Track B slot, with the row picked by a published teaser first,
  then the sequencing notes, then queue order.
- Found that his write allowlist would have forbidden the job. It named two files;
  a draft and its imageprompt are two more. Grew it to four, with the limit that
  he creates a draft and never edits an existing one.
- Set the new dates: stage 2 on Fri 28.08, Track B only, for the Mon 31.08 slot,
  with the Thursday story still written in a session. Stage 3, both tracks, no
  earlier than Fri 04.09.
- Gave the image style guide a home. `linkedin-posts/IMAGE-STYLE.md` is now the
  source a new imageprompt copies its header from; the copies stay and stay
  frozen. Reconstructed its history from the files rather than from memory: four
  versions, starting with a pen-and-ink chronicle look that belonged to the engine
  and not to me.
- Posted the report, scheduled the story, and flipped both rows the same evening.

## Technical Learnings

- A complete list of prerequisites can still miss the job. Three things were named
  on 12.08 as what drafting needs, and all three were right. The drafting workflow
  itself was on no list, because it had been described in prose in the same
  session that named the prerequisites, and prose reads like something that
  exists.
- A rule designed for one job does not reach the neighbouring one by being written
  down. One pull request per post was decided on 12.08 for drafting; the image job
  kept one per day and delivered two pictures in a single request as late as today
  — correctly, by its own spec. The batching defect of 07.08 had been answered on
  paper and was still live in the workflow it came from.
- An agent's question can find a missing structure rather than a missing value.
  What the underline colour should be took two seconds. Where the answer belongs
  revealed that the style guide had no location at all: sixteen copies and the
  convention that the newest filename wins.
- The same file cannot be source and record. A brief has to be self-contained for
  whoever generates from it, and an old brief has to keep describing the image it
  produced, so the copies are right. What was missing was the one file they are
  copies *of*.
- A boundary written as an allowlist has to grow with the job, and this time the
  allowlist was a real control — unlike "image files only" on 12.08, which read
  like one and was a sentence. Two files would have forbidden drafting outright.
- Adding a workflow multiplies the places the order is stated. It stood in three
  after 12.08 and stands in four now: the Abundly trigger, the numbered job list,
  the section layout and the recurring schedule. The trigger is the one that lives
  outside the repo.
- Cutting a paragraph can move a post's argument onto its pair's ground. Without
  the parallel-work beat, the report's case for handing over became the silence
  that the German story is about, so the week would have told one thing twice.
- English separates *responsible* from *accountable* and German does not. The
  distinction is exactly the one that matters when work is delegated to an agent:
  the doing can be shared, the answering for it cannot.

## Organizational Learnings

- The first thing Morten missed was a deadline, and it went unnoticed until
  somebody pointed at it. Where there is a gap in a process, a human will often
  step in to close it, and the process can be improved afterwards. Where an agent
  is involved who follows instructions rather than goals, that potentially does
  not happen.
- Morten has now asked instead of guessing twice, and both times the question
  exposed a defect in my own records: a contradiction inside his specification on
  12.08, and today a style guide that did not exist as a file. That was expected
  when the instruction was written, and it helps a lot in finding inconsistencies.

## Leadership Perspective

- Saying in the post itself that it was made together with AI and that I reviewed
  it was my own decision rather than a suggestion I accepted. I find it right and
  important. There is also official EU regulation now, the AI Act, Regulation (EU)
  2024/1689. Reading its Article 50 closely makes the decision sharper rather than
  weaker. The transparency duty for published text applies to content meant to
  inform the public on matters of public interest, and it explicitly does not
  apply where the content underwent human review or editorial control and a person
  holds editorial responsibility for it. For images it targets deep fakes, which
  stick-figure flipchart drawings are not. So the obligation is most likely
  discharged by the review before it arises, and the sentence in the post is a
  choice rather than a compliance step — which is the same distinction the wording
  turned on: the duty hangs on editorial responsibility, not on who did the work.
- Taking the slower path with the handover — stage 2 for the Track B slot only,
  when the tooling was ready for both tracks — comes out of having found twice
  now that too much was being done and tested at once.

## Other Learnings

- Morten is getting more complex, and so is everything around him. I am working on
  more fields at once — the corporate design, working with partners, learning
  nuggets, the learning journey, the posts — and it is easy to lose the overview
  there. It also tempts me to neglect quality and consistency, because first
  results can be celebrated so quickly. The cleanup work of the weekend — unifying
  the folder structure with Claude, using git repositories throughout, aligning
  the rules for those repositories, CRLF being the one to name, and pulling the
  content into line with them, defining rules for images and their originals — is
  what keeps good ideas and good results from turning into a rubbish heap, and
  what keeps quality and traceability intact.

## Open Questions

- How I make sure of quality as Morten takes over more subject areas.
- Whether his first draft holds up on 28.08. Stage 3 hangs on it.
- How I notice that he has not done something. The draft that should have come on
  21.08 went unseen until somebody pointed at it, and a gap nobody steps into
  stays open.
