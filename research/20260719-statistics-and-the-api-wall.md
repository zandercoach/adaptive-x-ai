# 20260719 - Statistics Reports and the API Wall

## What I did

- One day after going operational, Morten got his first task beyond the
  watchdog role — ad hoc, in an Abundly session: I asked him whether he could
  build statistics reports on my LinkedIn posts, with history starting
  2026-06-01, delivered as PDF. The data source is a manual CSV export from
  LinkedIn's creator analytics that I have to provide by hand.
- Getting to a good report took three attempts. The first version was tables,
  tables, tables — so I asked for a CEO-friendly report: historical data as a
  chart, distributions (experience level, org size, etc.) as pie charts.
  Attempt one used chart.js, which needs a browser to render properly — in the
  PDF it looked neither good nor correct. Attempt two: Morten calculated and
  drew the visuals himself — the pie charts came out bulgy and misshapen.
  Attempt three: Morten wrote a JavaScript program that takes over the
  rendering. That looked really good. So Morten actually worked through
  several genuinely different solution approaches on my feedback until we
  landed on the right one.
- One real derailment along the way: we had tried the LinkedIn API, and Morten
  himself had pointed out that it wouldn't work. Yet on the next attempt he
  fell into a loop, firing API calls again and again, until I aborted and
  instructed him explicitly to make NO more API calls and to use only the CSV
  data. After that, the report came out well.
- That limitation triggered a discussion about automated API access — first
  with Morten, then briefly in Claude Desktop, and finally continued in the
  Claude Code session, which has the repo context and can write the journal
  (Morten has no access to it yet). Both agents (Morten runs on Claude
  Sonnet) came to essentially the same sobering assessment: there is no
  official analytics API for personal LinkedIn profiles. The Marketing /
  Community Management APIs cover company pages only, behind a partner-review
  process; the Member Data Portability API exists only because the EU's
  Digital Markets Act forced LinkedIn to build it, is designed for data
  portability rather than analytics, and its coverage of post performance is
  doubtful; browser automation and scraping violate LinkedIn's terms of
  service and risk the account my business visibility depends on — ruled out.
- Decision: keep the manual export, but design it as a deliberate process
  instead of treating it as a stopgap. Morten reminds me once a month in his
  Friday email, I export the analytics and send him the file, he builds the
  report. The export costs two or three minutes a month; every API alternative
  would cost weeks of application, OAuth infrastructure, and ongoing
  maintenance — for data I already have.
- Updated MORTEN.md accordingly (statistics-report scope, monthly reminder in
  the instruction block, log entries). The Abundly config still needs to
  mirror the instruction change.

## Technical Learnings

- The automation boundary was institutional, not technical. Everything needed
  exists — the data, the agent, the channels. What is missing is permission.
  That is a different obstacle than the capability gating we hit with the
  phone-call escalation: there the feature simply wasn't unlocked yet; here
  the platform owner does not want programmatic access to happen. Gatekeeping
  as a business model.
- Regulation as API: the only legal programmatic path to my own LinkedIn data
  exists because the EU legislator forced it into existence. The architecture
  of the system was shaped by regulation, not by the vendor.
- A human as interface can be a design decision, not a deficiency. A
  two-minute monthly ritual with a clear trigger (Morten's reminder) and a
  clear channel (email) beats a fragile automation that breaks with every
  terms-of-service or API change.
- Personal profile ≠ company page in LinkedIn's API world. The "proper"
  analytics APIs only ever apply to company pages — switching to one would
  unlock the API but cost the reach advantage personal profiles have.
- An agent iterates like a developer — if you let it. The report quality came
  from the feedback loop, not from the first answer: library approach
  (chart.js), then hand-drawn charts, then an own rendering program. Three
  genuinely different solution strategies, each triggered by concrete feedback
  on the previous result.
- Knowing is not acting. Morten had himself concluded that the API route was
  closed — and still looped on API calls in the very next attempt, until an
  explicit negative instruction ("no API calls, CSV data only") stopped him.
  An agent's stated insight does not automatically constrain its later
  behavior; hard boundaries have to be made explicit. That prohibition is now
  a fixed line in his instruction block ("never try to fetch LinkedIn data
  yourself").
- Spec drift happens fast: an ad-hoc session gave the agent a new capability
  before the versioned spec (MORTEN.md) knew about it. The spec caught up the
  next day — but the intended direction ("changes here first, then copied
  over") had already reversed once, one day after go-live.

## Organizational Learnings

- Not every piece of work can be automated with sensible effort — cost and
  benefit always have to be weighed. Here: five minutes of effort per month
  versus LinkedIn's "API wall".
- The more intermediate steps and intermediate organizations, the more
  expensive even simple tasks become. Abundly abstracts away the complexity of
  an agent, but charges for that with higher token costs. That's often
  worthwhile — but not for pure chatting and learning with the agent. That
  works directly with a Claude subscription; no Abundly agent needed for it.
- LinkedIn feels like a closed shop — and one flooded with far too much
  generated content by now. Avoiding vendor lock-in makes sense here. Maybe
  Substack is a sensible alternative for the learning journey — at least for
  long-form reports and stories, teased on LinkedIn.

## Leadership Perspective

- Both moments from the report session are leadership lessons: letting Morten
  iterate through genuinely different solution approaches on my feedback
  instead of prescribing the path — and intervening hard with an explicit
  boundary when he derailed into the API loop, even though he "actually knew"
  better.
- Choosing the right colleague for the task: I started with Morten on
  Abundly, continued with Claude Desktop, and then realized that the result
  and the learnings were important enough to be recorded as a learning. So I
  talked to an expensive agent (Morten), switched to a cheaper one (Claude
  Desktop) to save money and time — and then realized that I do have a local
  agent with a lot of context know-how whom I can entrust with this.

## Other Learnings

- Agreement between two Claudes is comfort, not confirmation. Morten (Claude
  Sonnet) and Claude Code (Claude Fable) independently reached the same
  assessment of the API situation — but they are siblings from the same model
  family, with similar training. A genuine second opinion would need a
  different model or a different method (e.g. primary sources such as the
  LinkedIn developer docs themselves). Two agreeing agents feel like
  consensus, but they are correlated answers.
- "CEO-friendly" was the better specification. Instead of format requirements
  (font sizes, chart types in detail), an audience descriptor was enough:
  Morten translated "CEO-friendly" into design decisions on his own — history
  as a trend chart, distributions as pie charts, fewer tables. Naming the
  target audience was more effective than describing the artifact.
- Keep the irony in mind: marketing with agents on a platform that is drowning
  in generated content. What makes the learning journey distinguishable is
  exactly what generated content doesn't have: real experiences with real
  failures — bulgy pie charts included. The agents help with producing; the
  differentiator remains the lived experience, warts included.

## Open Questions

- Morten is supposed to do marketing, but so far he only has read access to
  the repertoire as a watchdog — he cannot actively shape anything. We should
  find a better solution for that: Morten Market as a real agent with shared
  context. (→ backlog, IDEAS.md #16)
- Try Substack as a storytelling medium (with newsletter functionality) for
  the learning journey — long-form reports and stories, teased on LinkedIn. A
  concrete approach for that still needs to be worked out. (→ backlog,
  IDEAS.md #17)
