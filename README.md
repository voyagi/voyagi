Developer tooling, plus the memory and MCP plumbing underneath AI agents. Mostly TypeScript, some Python.

## Upstream

[claude-glass](https://github.com/cadentdev/claude-glass) didn't work on Windows at all. Backslash path separators left every internal link unrewritten, and `serve` returned 403 for every file, because a containment check compared a backslash path against a forward-slash prefix. I reported it as [#28](https://github.com/cadentdev/claude-glass/issues/28) and fixed it in [#31](https://github.com/cadentdev/claude-glass/pull/31). That PR also carries two dependency XSS advisories, because the project's pre-push tests can't go green on Windows while those path bugs are there, so they had to land together. It shipped in [v0.7.8](https://github.com/cadentdev/claude-glass/releases/tag/v0.7.8)

Backslash path separators no longer break Windows builds (community contribution by @voyagi, #31, fixes #28)

The maintainer added CI in the same release, running the tests on Ubuntu and Windows. The Windows job [failed on pre-fix main](https://github.com/cadentdev/claude-glass/actions/runs/32321567161) and [passed on the branch carrying the fix](https://github.com/cadentdev/claude-glass/actions/runs/32321867418). Both runs are red overall on a separate dependency-audit job.

Claude Code is closed source, so what I send Anthropic is bug reports. Two became shipped fixes: deferred tools not reaching skills that run in a forked context ([#46654](https://github.com/anthropics/claude-code/issues/46654), fixed in 2.1.126), and the same CLAUDE.md loading twice on Windows when drive letter casing differs ([#19516](https://github.com/anthropics/claude-code/issues/19516), fixed in 2.1.47, where I brought the cost measurements and someone else brought the diagnosis).

## A few things here

- [claude-usage](https://github.com/voyagi/claude-usage) turns Claude Code's local session logs into a VS Code dashboard: tokens, cost, and how close you are to the rate limit, with no second API key to manage.
- [throughline](https://github.com/voyagi/throughline) is an auditable memory layer for incident response, where every recall comes back with a receipt, so "no prior incidents" can't quietly mean "the search broke".
- [datahub-blast-radar](https://github.com/voyagi/datahub-blast-radar) scores what a data change is about to break, by walking lineage through DataHub's MCP server and writing the verdict back into the graph.

The rest is side projects, templates I reuse, and forks I keep around. [taranity.com](https://taranity.com) is the studio I run.
