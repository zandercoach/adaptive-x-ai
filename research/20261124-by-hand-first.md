# 20261124 - By Hand First

## What I did

**Wanted to use AI-DLC, and asked how it works.** Who manages the agents, how many are there, and are they the same each time, so we could hold retrospectives? In AI-DLC v2.11.4 an engine picks the next stage, the main session conducts, and 14 agent roles are dispatched as fresh instances each time. It learns only from my corrections at its gates; a retrospective is not built in.

**A friend's post** described a retro with his agent team: a Scrum Master agent clusters what went wrong. They dropped estimates, because even the agents were way off.

**Compared the alternatives:** BMAD (closest to Scrum, with its own evidence-based retrospective), Spec Kit, OpenSpec, Superpowers, Ruflo. Claude recommended BMAD on the modernisation epic. I decided: first we do everything ourselves.

**The three majors by hand,** one pull request each: Jakarta XML Binding 4 (#24), Spring 7 (#25), JUnit 6 (Dependabot's own #22, rebased).

## Craft

- **A major version is a migration, not a bump.** JAXB 4 moved the packages from `javax` to `jakarta` (21 files, imports only). Spring 7 removed a method we called twelve times. JUnit 6 needed nothing.
- **When the test framework itself changes, green is not enough.** The same 35 tests had to run in the same five classes, and a deliberately tampered golden master had to fail.
- **What no test covers gets compared.** The real campaign generated with Spring 6 and with Spring 7 gave 391 identical files. That also covered the start of the Spring context, which no test touches.
- **A check is only as wide as its question.** "Nothing catches `IllegalArgumentException`" was too narrow, since a `catch (Exception e)` would catch it as well. I asked about tests and Velocity, and then every `catch` block was read.

## Leadership Model

- The post was a confirmation. In my friend's words: "Today we killed that rule. Even the agents have been way off for weeks now, so those estimates have little to no value. Yet I see so often that humans are expected to guess more precisely. Stop doing this. It won't work!"

## Operating Model

- First we do everything ourselves, because I want to understand technically why we do exactly what we do. In BMAD, as I understand it, I would see intermediate points and results rather than the reasoning.
- Retrospectives with agents are not needed for now. I work only with my pairing agent, Claude Craft, ask my questions the moment they come up, and need no dedicated retrospective.
