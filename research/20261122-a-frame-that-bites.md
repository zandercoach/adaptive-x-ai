# 20261122 - A Frame That Bites

## What I did

**Picked up the thread from this morning.** [A Chronicle in the Open](20261122-a-chronicle-in-the-open.md) ended on the frame that agentic coding needs and the engine did not have yet. In the afternoon it got one, in four pull requests on the engine.

**Less to guard first.** The legacy database path went — Hibernate, the DAOs, the converters, about 1,170 lines nothing ran and nothing tested (#12). Then the engine was formatted with google-java-format, checked on every build (#14).

**Gates that hold from the first day (#15).** Coverage, SpotBugs and PMD as ratchets: today's state is the baseline, only getting worse fails. Four architecture rules with ArchUnit. Then the frame written down (#16): a new `CLAUDE.md` with a Definition of Done, a public README, Dependabot. „Ratchet“ went into the glossary.

**One pull request went astray.** The formatting was stacked on the removal; it was merged into the removal's branch instead of `main`, and Claude deleted that branch while tidying up. Nothing was lost; it came back as #14.

## Craft

- **Dead code can carry live dependencies.** Removing Hibernate removed the JAXB runtime, which had only ever arrived through it, and `commons-cli`, thought unused, turned out to serve the third-party wiki parser. The tests caught the first, the compiler the second; generated output was compared byte for byte before anything went out.
- **A ratchet needs a measured baseline, and the baseline needs reading.** Coverage stood at 72 % of lines and 51 % of branches; SpotBugs found 81 things, 78 of them one pattern that JAXB models and Velocity beans follow on purpose. That became a policy with a reason, not 78 baseline entries. All four architecture rules held without exception, so they went in strict rather than frozen.
- **A gate counts once it has bitten.** Each one was shown to fail on a deliberate violation — a badly formatted file, a model using Velocity, `==` on strings, an unused field, forty uncovered lines — and green again once it was removed.
- **Stacked pull requests need their base branch deleted.** GitHub retargets a stacked request to `main` only then; otherwise the merge lands in the base branch. Now every request goes straight onto `main`, head branches are deleted on merge in all four repositories, and `CLAUDE.md` says so — along with commits only when asked, after Claude had committed locally without asking.

## Business Model

- The frame is proof of agentic coding for trainings. It will certainly change and grow; what matters is to think it along from the start and keep it up.

## Leadership Model

- The frame should be as precise as possible, so that violations surface early and do not multiply. Mistakes may happen, but they have to be correctable. A frame cannot foresee every eventuality, so mistakes have to surface, and then be correctable.

## Operating Model

- The CI takes the checking of the basics off me. What else the frame brings with it, I will try out and learn over the coming weeks.

## Open Questions

- The Velocity update is open: the engine still runs on Velocity 1.7.
