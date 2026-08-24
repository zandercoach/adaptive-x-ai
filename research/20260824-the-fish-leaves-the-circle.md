# 20260824 - The Fish Leaves the Circle

## What I did

- Started a corporate design for zander.coach from the only asset that existed:
  a 563 px PNG of the logo. Answered seven decision questions (scope, whether the
  old website draft was a basis, how much the mark could change, which
  positioning stage the design should show, character, surfaces, languages)
  before any design work started.
- Found vector sources — an Affinity EPS and PDF from 2021 with all letterforms
  already converted to outlines — and derived clean SVGs from them. Two findings
  from measuring: the signet was 1.16 % wider than tall, an export artefact, and
  the brand petrol `#008888` reaches only 4.19:1 on white, short of the body-text
  threshold.
- Named what the mark means, which had never been written down anywhere: a fish
  leaving the circle to the left, with only the tail fin still visible. The form
  is made of what is already gone. That produced the design's governing rule —
  the appearance must never look like it wants to stay.
- Drew a set of hand elements on ten sheets and had them cut into 58 transparent
  PNGs — arrows, dividers, braces, highlighter strokes, numbers, states,
  thirteen pictograms, four hand-drawn signets, a signature, and a complete
  hand-drawn Scrum flow.
- Threw the source sheets away, then recovered them from the recycle bin after
  hearing the argument: the derived files are capped at 1600 px, and a wrongly
  cut element cannot be re-cut without the source. Both had already happened
  once in this session.
- Chose direction B, then switched to C because the website's leading idea is
  "When the structure does not carry" — which made the choice a matter of content
  rather than taste. Then turned the whole thing into an A/B test with both
  directions carried to the same finish.
- Reviewed a partner training programme (Leading Mindfully, with Ingo and
  Matthias) and let Claude write ten reasoned improvement proposals.
- Built two slide decks describing the training series, one per design direction,
  from a single content source so their text stays provably identical.
- Converted the website draft to the chosen system and generated the second
  variant from it by script, for the same reason.

## Technical Learnings

- An EPS from Affinity is plain ASCII PostScript with only `moveto`, `lineto`,
  `curveto` and `fill`. No tracer needed — a 40-line parser converts it to SVG
  losslessly. 97.7 % pixel overlap against the original PNG, the rest antialiasing.
- Extracting ink from photographed paper needs illumination normalisation
  (divide by a heavy blur) **and** saturation, or a green highlighter falls
  through the brightness threshold entirely.
- The same method destroys large filled shapes: for a solid disc the local
  background estimate is itself black, so the interior becomes transparent. Those
  need a global paper-white estimate instead.
- Flexbox silently shrinks zero-height decorative elements to nothing when a slide
  is tight. A signature design device was missing from several slides and the
  defect was invisible at thumbnail size — `flex: 0 0 auto` fixes it.
- `pathLength="11"` with `stroke-dasharray="1 1"` produces exactly six dashes
  whatever the curve's real length, and — unlike `pathLength="12"` — ends on a
  dash rather than a gap.
- An SVG `marker-end` with `orient="auto"` aligns an arrowhead to the path's end
  tangent. A hand-placed chevron drifts out of alignment the moment the curve
  changes; the marker cannot.
- Container queries (`cqw`) make true-to-scale mockups: A4, 16:9 and 1:1 surfaces
  that keep their proportions at any viewport width.
- A headless screenshot can catch a CSS entry animation mid-flight and look
  exactly like a colour bug — grey headline, invisible buttons. It was a
  measurement error, not a defect. `--virtual-time-budget` settles it.
- For an A/B test, generating both variants from one source is not tidiness, it
  is the validity condition. Two hand-maintained copies drift on the first edit,
  and nobody notices.

## Organizational Learnings

- Giving design work to an agent was rapid from idea to prototype, and slow from
  the prototype to a better, by far not "finished" corporate design. In creative, 
  visual work a lot of things in the result turn out well-meant but not necessarily
  coherent and consistent. Closing that gap still demands know-how of my own, which
  I do not have, and time of my own, which I do not have either. The classic
  prototype dilemma.
- The question this raises is who does that creative work. "Simple" work can be
  taken over well by AI — but who does the "complex" work? A good example of why
  automation must not lead companies to neglect training the people who later
  have to take that work over as seniors.
- Answering seven decision questions before anything was designed gave me a first
  overview of the whole frame and helped me orient myself as a layman.

## Leadership Perspective

- Revising the direction twice was quickly done, because a revision here is not
  tied to any cost. What is missing on the other side is the friction that
  working with a person brings, and that in conversation very often leads you to
  new ideas and solutions.
- Producing the A/B test as a follow-up job was easy: as long as a shared basis
  is used — here the deck source — Claude can do it almost entirely alone, with
  the Pareto problem that the fine points do take a lot of feedback and adjusting.
- As the client you are confronted with less mature states and get to engage with
  that, to give feedback more actively — and possibly to have to bring more
  knowledge of your own. Whoever does not have that will have to live with a
  result that is not optimal, or will need a senior at their side.
- What made me change the decision to throw the source sheets away is that in
  creative processes it is always good to keep the originals, so that other
  derivations for the design can still be made from them later. That is why I did
  not delete the photos — and afterwards carried the insight over to the other
  originals.

## Other Learnings

- The meaning of the signet existed only implicitly in my head; it took Claude to
  make it explicit. Until now I had never used it explicitly and never had to
  explain it. The reading — more clarity by taking away — was something Claude
  worked out first; I had not seen that interpretation before at all.
- A design question turning into a question of content was coincidence. I am not
  a designer and did not approach the topic that way, neither in content nor
  creatively. And then Claude's argument was coherent.

## Open Questions

- The appearance and the A/B test are only a first step and not yet mature enough
  in quality. There is still a fair amount I would want to change.
- Whether the design carries over to the platform it has to run on. Ingo and
  Matthias report that a corporate design as a prototype is well within reach with
  Claude, while carrying it over to a WordPress website is not easy to do with
  Claude's support. Technical expertise seems to stay required there.
