# 20260831 - Mechanism Beats Rule

## What I did

- Wrote the journal entry for the 30.08 session, sections 1-2 from that evening's
  commits and 3-6 from an interview. Titled it *The Review Is the Work* after my
  own answer in it: the handover moved the work rather than taking it away,
  because reviewing is the work.
- Ran the curation pass on `REPERTOIRE.md`. Sixteen open Track A rows became
  eleven through five merges, each into an umbrella that already carried the same
  message: A44 into A28, A41 into A25, A38 into A20, A37 into A35 (retitled *Der
  Stuhl des Auftraggebers ist nicht der billige*), A42 into A40. Track B stayed at
  six, since the 30.08 session is not harvested yet and B would have grown again
  in the same week. Two further merges were weighed and rejected with reasons.
- Made brevity a rule. Everything Claude writes for me — answers, commit
  messages, specifications, instruction blocks — is to be short and to the point,
  after the instruction block lost a third of its words with no rule dropped. It
  went into the workspace root beside the voice cascade, because it holds across
  all areas and is a different axis from `VOICE.md`: how Claude writes, not how I
  sound. Morten got his own copy as a third thing asked of him in every job,
  because he does not read the root.
- Asked Morten how we could stop mirroring his instruction block by hand, and
  took his answer: the copy becomes a build artefact. `spec-sync` extracts the
  block on every push to main that touches `MORTEN.md` and writes it verbatim
  into an agent document he reads on every run. Abundly's instructions shrink to
  a stub — identity, two cron lines, two quoted boundary sentences, a no-spec
  rule. He had built the handler and the guards before asking; what he could not
  do was touch `agents/`.
- Added the `morten-spec` markers outside the fences, so his heading-based anchor
  kept working and the switch could happen in either order. He has since switched
  to the markers and kept the old reading as a fallback that announces itself in
  #crew when it is used.
- Wrote the coupling above the fence rather than leaving it in his code: the stub
  quotes two sentences of the file verbatim and the sync compares them on every
  run, so editing either sentence starts a daily drift message until the stub is
  pasted again.
- Took two corrections from him on my own prose. The stub carries a *no-spec*
  rule, not an unreachable-repo rule — with GitHub gone the last good copy is
  still in the document, which is what it was built for, so the block's rule
  governs there, mail and subject line included. And "the hard boundaries" is
  shorthand: it is two quoted sentences, not all five.
- Pushed four times, refreshed the mirror twice, and let the first sync fire on a
  real push.

## Technical Learnings

- A copy nobody edits by hand is not a second record. The mirroring rule had hung
  on somebody remembering it since 19.07, and it failed in that exact way three
  times. A generated copy cannot drift silently — the failure mode changes from
  invisible to noisy.
- A quotation drifts as surely as a paraphrase, only later: the moment the quoted
  sentence changes in its source. That is why the check is a comparison rather
  than a copy, and why the coupling belongs above the fence — a cost nobody sees
  is a cost nobody budgets for.
- A fallback that does not announce itself becomes the normal case in silence.
  Morten's marker fallback says in #crew when it is used, which is the same shape
  as the daily run behind the webhook: the net has to leave a trace.
- The comparison belongs before the work, not after it. His daily trigger points
  at the sync rather than at the review loop, so a stale spec cannot serve one
  more run before being noticed.
- An unreachable repository and a missing specification are two different
  failures with two different floors, and naming them the same thing hides the
  one case the stub exists for.
- An enumerated order inside a trigger is a second copy in miniature. The Friday
  line listed five workflows; a sixth would have made the stub prescribe the
  wrong order. It now names the specification instead of repeating it.
- Two copies were made today and one was abolished, and the difference is who
  writes them. The generated block ends the hand-mirroring; the brevity rule was
  deliberately written twice, in the root and in `MORTEN.md`, because Morten
  cannot read the root. A copy is only safe when a machine writes it or when the
  reader of one cannot reach the other.
- Merging queue rows only works into an umbrella that already carries the
  message. Five did; the two that were rejected would have joined rows whose
  message is a different one, which is the same line as 17.08.

## Organizational Learnings

- What made Morten's answer useful was that I described the target state and not
  the solution. He came back with sensible proposals, and we worked through them
  together.
- Morten reading my records back and finding the defects in them is something I
  deliberately do not rely on, and it helps a lot. He also seems to know his own
  environment better than Claude and I do.

## Leadership Perspective

- Replacing a rule with a mechanism wherever it can be done is deliberate:
  mechanism beats rule.
- Where that stops is not a line I have drawn on purpose: I do not yet know all
  the mechanisms we could use to replace rules with.

## Other Learnings

- A day that produces no post and goes entirely into the journal, the queue, the
  rules and Morten's spec is a necessary investment. Without it everything decays
  into chaos and legacy — and it automates working steps and makes me more
  effective on top.

## Open Questions

- Which mechanisms exist that could replace a rule. I do not know them all yet,
  and that is what limits how far *mechanism beats rule* actually reaches.
- Whether the brevity rule arrives in what Claude writes, or only stands in the
  file that says it should.
- Whether eleven open Track A rows are curated, or only fewer than sixteen.
