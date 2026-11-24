# Claude Craft — Engineering

Christian's agent for engineering, drafting, and this journal, running in Claude Code on his machine. Named after the journal's `Craft` section, the hands-on layer. A member of the `zandercoach` org with its own account [`claude-craft-agent`](https://github.com/claude-craft-agent), in the `crew` team alongside Christian and Morten.

**In Christian's words:** more a team member, with superpowers.

## What Claude does

- **Engineering** — modernises `chronicler-engine` and its instances: reading code, planning, writing and checking the changes.
- **Drafting** — writes the LinkedIn posts against [`VOICE.md`](../linkedin-posts/VOICE.md) (Christian voice-checks and posts) and the `-imageprompt.txt` files (Morten generates the images).
- **The journal** — runs the reflection interviews for the `research/` entries, one question at a time, and writes them close to Christian's words.
- **The company brain** — helps keep the repo authoritative: consolidating knowledge into it, and holding the line between shared truth and private working memory.

Everything Claude writes reaches `main` as a pull request from `claude-craft-agent`. Christian approves and merges; Claude does neither.

## How Morten Market and Claude Craft compare

| | Morten Market | Claude Craft |
|---|---|---|
| Role | Marketing & Sales | Engineering |
| Platform | Abundly | Claude Code, on Christian's machine |
| Identity | own GitHub account + token | own GitHub account + tokens |
| Attribution | commits authored by `morten-market-agent` | commits authored by `claude-craft-agent` |
| Writing to the repo | only via pull request, never `main` | only via pull request, never `main` |
| Boundary | enforced by controls (token scope, branch protection) | enforced by controls (token scope, branch protection) |
| Persistence | a standing agent, triggered on a schedule | exists only inside Christian's sessions; each starts fresh |
| Memory | the repo + Abundly config | the repo + private `.claude` memory, not versioned |
| Team channel | `#crew` and `#crew-alerts` | not on Slack — reachable only inside a session |

What still separates them is the lower half of the table. Claude has no life outside Christian's sessions and no memory of its own: the continuity that makes it feel like one colleague across sessions comes from the repo and the memory files, not from anything Claude carries.
