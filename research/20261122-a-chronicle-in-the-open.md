# 20261122 - A Chronicle in the Open

## What I did

**The Chronicler got a pipeline (20.–22.11).** Every push and pull request on the engine now builds and runs the tests: a golden master over seventeen generated pages and five invariants every page must keep. `main` is protected; each change came as its own pull request.

**The test fixture became a story.** Placeholders like `Test-Member` gave way to *Der verlorene Zehnt* and *Der Turm im Nebelmoor*, German throughout, because looking at the pages made me want them to read like a chronicle.

**What was hardcoded became instance configuration.** Title, welcome text, copyright, wiki source and icon, imprint and privacy links, the map and the calendar now come from the data repo. The home page reads its heroes from the data; a hero with a status has retired and keeps only their own page.

**Two instances, two ways out.** The campaign is checked against its real data on every push and uploaded over SFTP to dsa.zander.coach, replacing a site from April 2025. The new public demo at [chronicler.adaptive-x-ai.org](https://chronicler.adaptive-x-ai.org) publishes itself through GitHub Pages: its own calendar, eighteen pictures in the flipchart style drawn from Claude's briefs, no Google map. This site links it and now says how I learn.

## Craft

- **The golden master turns review into decisions.** Seeing the generated pages, not the diff, is what made me ask for real names, a German fixture and a configuration per instance. The approved copy then showed exactly what each of those changes touched.
- **A test against real data can find a bug in the test.** Run against the campaign, one invariant reported an event as missing: its title held a wiki link, and the test compared the raw text with the rendered one.
- **The first real upload stopped at an umlaut.** The deploy script read the server's file list in the Windows code page and could not delete `kreatur_Krähe.html`. Uploading first and deleting after kept the site whole while it failed.
- **Defaults that protect, or stop.** Google Maps loads only where an instance switches it on; without a calendar the generator stops with a message instead of falling back to DSA.

## Business Model

- The Chronicler in the open matters to me personally, and it is proof that I am not only dealing with AI but with agentic engineering and agentic coding. It will flow into a new training on agentic coding, and it serves as proof when acquiring new project engagements.

## Leadership Model

- In agentic coding, goals are more helpful than step-by-step instructions — within an appropriate frame that ensures code quality, maintainability and extensibility. Much of that frame is still missing; building it will be the next steps. On the other hand I can build on the frame I set up for my website, which makes some things in the presentation layer faster.

## Operating Model

- The current setup is still somewhat cumbersome, and that is partly due to the setup itself: one engine, one public demo, one "real" instance. I will give it more thought.

## Other Learnings

- Compared to my first steps — the beginning of this journal, where I struggled with token limits and compacting because the work packages were too big — things run much more smoothly and with fewer errors, in smaller packages and with a newer model, Opus 5.5.

## Open Questions

- The route view needs a solution of its own, for example via avesmaps.de.
- I want to try an agentic SDLC, or even an AI-DLC (AI-driven development lifecycle).
