# 20260731 - The First Resource: AI for Leaders

## What I did

- Filled the Learning Resources page that had gone live empty two days earlier,
  with the source that had been sitting at the top of its inbox: "AI for Leaders"
  (Level 1) by the Agile Academy, facilitated by Sohrab Salimi — a fellow trainer
  and a mentor of mine. Normally a two-day training; for the ambassador cohort it
  ran as four afternoons, 21/22 and 28/29 July.
- Checked what the material actually permits before writing a line about it. The
  deck is licensed CC BY-NC-ND 4.0: free to share with teams and clients, but
  public republication needs a licence from the Agile Academy — and this repo is
  public republication. My own premise going in ("darf nicht publiziert werden")
  turned out to be too strong: I may share it, I just may not publish it. The
  96 slides stay outside the repo, at
  `C:\projects\zander.coach\LearningResources\AIforLeaders\`.
- Solved the ingestion on the way: `Read` cannot render PDFs on this machine
  because poppler isn't installed. The working route was a virtual environment in
  the scratchpad plus `pypdf` text extraction — enough to work from, and worth
  reusing.
- Wrote the entry in the shape all later ones will follow: a facts table, a
  factual "what it argues", and the three handwritten fields — what I took from
  it, where it landed, the verdict — interviewed one question at a time.
- Extended the entry contract in `RESOURCES.md` twice, because the first real
  entry showed what the skeleton was missing: a **Source material** field, so that
  where a source sits and what its licence allows is stated instead of leaving a
  missing link as a mystery; and the rule to characterize rather than reproduce
  **even where a licence would allow more** — the value of an entry is the take,
  not the material.
- Recorded what the training confirmed and what it added. Confirmed: AI is
  infrastructure rather than IT, delivery gets faster and more compact down to
  "1 + AI" teams, and leadership moves back close to value creation. Added as
  explicit points: don't outsource AI, because it has to become part of the DNA of
  the core business — and how deep to take AI into your own hands (application,
  model, or infrastructure layer) is a real decision about sovereignty.
- Traced where it had already landed, and found one influence that is datable
  rather than remembered: the line about being "back in the game as a
  player-coach" entered `team/christian-zander.md` on 28.07 — the same afternoon
  the training covered the model, and before the source was named anywhere in the
  repo. Not a coincidence; the entry says so.
- Named the other landings: Morten as an agent on Abundly and as part of a team
  (the training runs on Abundly too — the Agile Academy is their first worldwide
  partner), and the move to *one* core team rather than a marketing team,
  "1 + AI" for now and maybe "2 + AI" later. That one turned into work the same
  evening.
- Left a moonshot in the entry as a commitment: I will check the learning journey
  itself for business-model viability, the same way I check my existing business
  and the repositioning — and probably the Chronicler as well.
- Committed and pushed the entry (`f79efff`), source file and rendered page
  together.

## Technical Learnings

- Check the licence before designing the entry, not after writing it. The licence
  is what determined the shape here: because the deck cannot be republished, the
  entry had to be able to say *where the material sits and why there is no link* —
  which is exactly the field the skeleton didn't have.
- "Characterize, don't reproduce" is the stronger rule even when the licence is
  permissive. Tying the rule to permission would have made every entry a
  negotiation with a licence text; tying it to the purpose of the page settles it
  once — the take is the content, the material is the citation.
- A format is only tested by its first real instance. Two days of designing the
  skeleton produced a good structure and still missed two things, both of which
  became obvious within an hour of having actual material in hand.
- PDF ingestion on this machine has a working route and a broken one: `Read`
  needs poppler and fails, a scratchpad venv with `pypdf` extracts the text fine.
  Python is there; poppler is not.
- A versioned repo makes influence provable instead of remembered. The
  player-coach line is timestamped in git, three days before the source was named
  anywhere — so "this training changed something" is a fact in the history, not a
  reconstruction after the fact. Committing thinking as it happens turns the repo
  into an audit trail of one's own head.

## Organizational Learnings

- That the coordinating manager role loses its reason to exist as the
  value-creating unit shrinks to "1 + AI" is a statement about structure and
  about speed at once — but above all about speed.
- What makes that speed possible here: there is nobody to convince but me, and
  the structure costs almost nothing to rebuild — rename a team, two Slack
  channels, one instruction block. Three days from the training insight to the
  org chart.
- In larger organizations this becomes a real challenge. It threatens the status
  quo, it threatens the power structure and the standing of the people inside it
  — so both subversive and open resistance are to be expected.

## Leadership Perspective

- Having the Player Coach model put a name and a source on what I had only
  thought intuitively makes me more certain, not less: the model confirms what I
  already live.

## Other Learnings

*(nothing beyond the sections above this session)*

## Open Questions

- Sovereignty is open: how deep to take AI into my own hands — "only" the
  application layer, or the model layer, or even the infrastructure layer.
- The moonshot is open: whether this learning journey itself is viable as a
  business model, checked the same way as the existing business and the
  repositioning.
