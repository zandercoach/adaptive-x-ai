# 20260718 - Drafts, Schedules, and Morten Market

## What I did

- Wrapped up the week's posting arc first: B3 "teaching the AI to sound like me" went out Monday 13.07, and A1 "Kontext verloren" went out Thursday 16.07 — after I had reframed it (session of 14.07): the original message "cut work into smaller packages" felt Tayloristic for knowledge work, where you lead by bigger or smaller goals. The new frame is situational leadership, with my own misjudgment as the confession: I treated the agent like a senior (delegating) when, for that refactoring, it was a junior that needed telling or selling. "Enger führen statt Delegieren."
- Drafted the next two posts from the repertoire. The B1 journey report "The big rename" needed a factual correction: the first draft read as if the agent had done the refactoring. It hadn't — it hit the token limit and lost the session, so I did the refactoring myself in Eclipse, class by class, chasing hardcoded references; the agent did the directory renames, the GitHub repos, and the cross-checks. I missed some references anyway, which produced correct files with broken links and images — the characterization tests caught the structure but not the content. Content-level tests are now on the list.
- Reworked the leadership part of the A2 story "Selbstbewusst ist nicht richtig" myself: the questions I actually use as Führungskraft and as facilitator, instead of a generic translation.
- Generated the flipchart images and scheduled both posts in LinkedIn's own scheduler (B1 for Monday, A2 for Thursday). That changed the reminder problem: "don't forget to post today" is solved natively — what needs watching is the queue running dry upstream.
- Turned the planned reminder agent into something bigger: Morten Market, my marketing agent, named in remembrance of the lead singer of a-ha. Hosted on Abundly (Henrik Kniberg's agent platform) instead of a Claude Code cloud routine. MVP scope is a queue watchdog: every Friday 08:00 he reads the public REPERTOIRE.md, mails me a status verdict, and escalates to the #marketing channel in my Slack workspace only if the coming week is empty. Escalation was planned as a phone call, but that capability would have required contacting Abundly support — Slack it is, which needed a dedicated Slack app for the agent. The spec lives in the repo as MORTEN.md, the versioned source of truth the Abundly config mirrors.
- Tested everything end-to-end: email, Slack escalation, the full queue check, and the Friday trigger. Morten is operational; his first scheduled run is Friday 25.07.

## Technical Learnings

- A post series accumulates factual debt. The second post touching the token-limit event nearly shipped a wrong division of labor ("the agent refactored everything"). The fix wasn't just editing the draft: the corrected facts went into the REPERTOIRE.md source column, so the queue file now doubles as fact memory for future drafts.
- Check what the platform already does before building automation around it. LinkedIn's native scheduler dissolved half the reminder agent's job before it existed; the remaining job (watch the drafting rhythm) is smaller and better defined.
- Host an agent where its outbound channels are first-class. The Claude Code cloud-routine design could only create Gmail drafts and calendar events — workarounds. Abundly sends email and posts to Slack natively, and the whole contact-channel problem disappeared.
- A public repo works as a credential-free API between AI systems. Morten needs no tokens or keys: REPERTOIRE.md, VOICE.md, and even his own spec are public raw URLs. One agent (Claude Code) writes the state, the other (Morten) reads it; the markdown file is the interface.
- Encoding an external agent's config as a versioned repo file (MORTEN.md, mirroring the same pattern as VOICE.md) keeps the platform config reviewable and reconstructable — the platform UI holds a copy, the repo holds the truth.
- Capability gating is a real design force: the phone-call escalation died on "requires contacting support" and became a Slack message. Designing the escalation as a separate, swappable step made that a one-line change instead of a redesign.

## Organizational Learnings

- Morten Market keeps an eye on the LinkedIn posts for now, but is meant to grow into a marketing agent — work I don't enjoy doing anyway. So effectively I'm hiring someone and training him in, so that I can concentrate on the work that is more appealing to me — and the work where I can generate the most value.
- The communication channels are clearly defined, both for the normal case and for the escalation case. That makes "distributed" working — me at home, Morten in Sweden at Abundly (probably somewhere in the AWS cloud) — well and effectively possible.

## Leadership Perspective

- Morten's goal and task were the entry point. But because I don't know him yet (and AI agents in general, for that matter), I deliberately started small, so that we can become familiar with each other first. And at the beginning, many things were explicitly worked out and clarified — including by directly asking Morten what he needs to do his job in a meaningful way. That's how a way of working together emerges in which trust can grow — and with it, the expansion of his authority and his responsibilities.
- Explicit communication channels help avoid misunderstandings and support effective collaboration — especially important when you don't meet "live" every day but work distributed, across locations, countries, and time zones.

## Other Learnings

- Agent literacy is portable. This was the journey's first step outside the Claude world — and nothing important had to be relearned. The discipline acquired leading Claude (goal, context, boundaries, explicit channels, start small, verify) transferred directly to configuring an agent on a completely different platform. The skill isn't "using tool X", it's leading agents.
- A name changes the relationship. "Morten Market" is not decoration. The moment the agent had a name and a job title, the work stopped feeling like configuring a cron job and started feeling like hiring: writing a job description, defining reporting lines, deciding what he may and may not do. That framing produced better design decisions — and it's more fun. (Footnote for the record: a-ha are Norwegian, but Morten now lives in Sweden, at Abundly.)
- One event, two audiences, zero extra material. The token-limit crash became two different posts from one set of facts: a German leadership story about situational leadership, and an English lab report about the division of labor. The journal entry was written once; the angles did the rest. The repertoire multiplies material instead of consuming it.

## Open Questions

- How does Morten grow from watchdog to a real marketing agent?
