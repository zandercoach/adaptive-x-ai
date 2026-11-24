# 20261124 - The Suit Gets an Account

## What I did

**Wanted merges that are not blocked.** Every pull request Claude opened ran under my login, and GitHub lets nobody approve their own; branch protection asks for one code-owner review, mine. So every merge went through the admin bypass.

**Claude got its own account.** `@claude` and Claude Approvals did not fit a local session. Instead a machine account like Morten's: Claude Craft, `claude-craft-agent`, named after this journal's Craft section. Claude Debuggy, after Debussy, lost. Member of `crew`, two tokens.

**First approval instead of bypass.** Engine #27 was the first merge with my approval on a pull request Claude had opened. The team page, the site and Morten's briefing followed (#28): the "honest asterisk" is gone. Claude works in this repo by pull request too now.

**Not on Slack, on purpose.** Claude advised against it for now: it exists only inside my sessions, where I already sit beside it (IDEAS #29).

## Craft

- **The author of the pull request decides who can approve, not the author of the commits.** A `Co-Authored-By` trailer is text, not an identity.
- **One agent, two tokens.** The org refuses classic tokens, and a fine-grained token cannot reach a private repo where the bot is only a collaborator. Both are used per command, so my own login stays untouched.
- **Proof is a real push, not a permission field.** The API showed push rights while the token still waited for the org's approval.

## Leadership Model

- The bypass felt "red" and like an emergency, every time — very irritating. Approving a pull request from Claude Craft is an orderly process instead.
- I actually look into Claude Craft's code more than I used to look into the changes I committed myself.
- Morten and Claude stand on one level in the team for me — one as an agent on Abundly, the other as an assistant on my local machine. That is why they are named alike: "Morten Market and Claude Craft", or "Morten and Claude", never mixed.

## Operating Model

- In this repo too, I expect to look at the changes more closely than when I simply allowed them myself with my godlike power.

## Open Questions

- Whether an agent with its own identity changes what I sell or show in trainings is open; so far only the GitHub mechanics have changed.
