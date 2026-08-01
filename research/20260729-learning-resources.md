# 20260729 - Learning Resources

## What I did

- Opened a new front on the journey: the learning that happens *outside* the
  sessions — books, videos, webinars, articles, trainings — had no place in the
  company brain at all. Everything the repo knew, it had learned by doing.
- Set up the structure for it before there was any content: `RESOURCES.md` in the
  repo root as the source of truth, `docs/resources.html` as its rendering in the
  site's existing visual system, and a link from "Follow along" on the index page.
- Decided it is a **complete log, not a recommendation list**. Sources that turn
  out to be a waste of time stay in, labelled — that is the more useful signal,
  and it fits a journal that already publishes its wrong turns.
- Grouped the log by the three models from the working hypothesis — business,
  leadership, operating — plus a fourth theme for craft, since the agentic
  engineering material doesn't belong under any of the three. A source may sit in
  more than one.
- Split every entry into two layers with different authors: the facts (title,
  author, format, link, what it argues) may be agent-drafted, while *what I took
  from it*, *where it landed* and *the verdict* are mine, interviewed one question
  at a time. That is the journal's own division of labour, applied to reading.
- Established what can actually be ingested, before promising anything: articles,
  PDFs and my own notes are reachable; YouTube only via `yt-dlp` auto-captions,
  which isn't installed on this machine (Python is); webinar recordings and gated
  trainings are not reachable at all. Books are never scraped.
- Shipped it empty. `RESOURCES.md` went out with an inbox of two named sources —
  the Kniberg webinar from 17.06 that started this whole journey, and the "AI for
  Leaders" training that had ended that same day — and nothing written about
  either. The content was promised for the evening; the skeleton was committed
  and pushed on its own (`ae78d0c`).

## Technical Learnings

- Where a source *sits* is a design decision, not an afterthought. Deciding the
  ingestion routes first meant the page was designed around what is genuinely
  reachable, instead of promising a completeness that would quietly rot into
  half-filled entries.
- For the unreachable sources — the gated training, the webinar recording — there
  is no technical route and none is coming. I am the sensor. The structure has to
  be built for a human input channel as the normal case, not as the degraded one.
- "Nothing here yet" is a valid published state. The alternative — holding the
  page back until it had content — would have meant the structure and the first
  entry arriving as one lump, with no way to tell which decisions were about the
  format and which were about the material.
- The two-layer entry needs the rule written down next to it, or the agent layer
  will quietly grow into the human one. `RESOURCES.md` carries its own
  "rules of the house" for exactly that reason: never write the take from
  inference, and half an entry is honest where an invented take is not.
- Rendering from a markdown source into the existing site system cost almost
  nothing, because the visual system was already there to copy from. The page is a
  second view on a repo file, not a second place where the content lives.

## Organizational Learnings

- This learning journey is meant to be an inspiration for anyone interested — and
  if that is the point, then the *sources* of the learning are as interesting to
  them as the learning itself.
- Transferred to an organization: valuable sources of learning should be
  available to everyone, not held privately by whoever happened to find them.
- Mistakes — including mistakes in *choosing* a source — should be visible as
  mistakes and celebrated as such, to establish a proper learning culture. That
  is what the complete log is for: the duds stay in, labelled.

## Leadership Perspective

- Letting an agent write the take — what I took from a source, where it landed,
  the verdict — would fail on both counts: it couldn't do it well, and more
  importantly it would stop being *my* learning journey. I want to stay involved
  here, and to lead by example.

## Other Learnings

*(nothing beyond the sections above this session)*

## Open Questions

- I want to use YouTube as a source, but it still has to be made technically
  possible — `yt-dlp` isn't installed yet.
- Summaries of the *content* of books would be helpful too, as long as they are
  legal to produce.
