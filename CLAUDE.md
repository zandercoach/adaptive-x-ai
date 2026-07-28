# Instructions for Claude Code working in this repo

This repo is **our company brain** for the "Adaptive × AI" learning journey (see README.md for the why): the shared, versioned source of truth that everyone on the team — human and agent — reads from and can rely on. It is the *long-term, reviewed* layer of that brain — durable facts, decisions, conventions and the journal — not a place for working state. Each member keeps their own private working memory outside the repo (Claude's session memory, Morten's Abundly context); only what is reviewed and shared belongs here. It documents the *journey*, not the code — the actual project being modernized along the way lives in separate repos (`chronicler-engine`, the public engine, and `chronicler-data-cfk`, the private content).

## Structure

- `research/YYYYMMDD-topic.md` — one entry per session or topic, oldest first by filename.
- Each entry uses a fixed six-section template:
  1. `## What I did` — factual recap of what happened in the session.
  2. `## Technical Learnings` — technical/process lessons.
  3. `## Organizational Learnings` — how the work of building/collaborating changed.
  4. `## Leadership Perspective` — reflections on directing an agent vs. leading people.
  5. `## Other Learnings` — anything that doesn't fit the categories above.
  6. `## Open Questions` — what's still unresolved.

## Filling in an entry

Sections 1 and 2 (`What I did`, `Technical Learnings`) can be drafted directly from session history — they're factual and observable.

Sections 3-6 (`Organizational Learnings`, `Leadership Perspective`, `Other Learnings`, `Open Questions`) are Christian's personal reflection. **Never invent or paraphrase these from inference alone.** Ask him directly, one question at a time, waiting for his answer before asking the next. Write his answers close to his own words — light cleanup for readability is fine, rewriting his voice is not.

When you write his answer into a reflection section, make it a **self-contained statement, not a reply.** Drop the conversational opener ("Both, actually", "Yes, because…") and put back the thing it refers to, so the bullet stands on its own when the entry is read later without the interview around it. Everything after the opener stays close to his words. E.g. "Both at once" becomes "Giving write access was both at once — giving trust and installing a safeguard — and the safeguard is what made the trust cheap."

## Working in this repo

- Before updating or referencing an entry, read its current file content — don't rely on memory of what it used to say, since it changes across sessions and may have been edited directly (by Christian or a linter) between sessions.
- New entries follow the existing template exactly (same six headings, same order) unless Christian asks to change the template itself.
- Commit only when explicitly asked. Push only when explicitly asked — this is a public repo.
