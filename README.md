I build small tools and services, mostly in TypeScript, some Python. Each one starts from a written spec of what "done" means, and I test it against that spec until it holds.

## Projects

- **[Plainletter](https://github.com/voyagi/plainletter)** won third place (Bronze) in the Good Neighbor track of a hackathon on Devpost in October 2026 ([the result](https://devpost.com/software/plainletter)). It helps the volunteers at a free help desk read an official letter with the person who got it, and checks every amount, date and reference against the letter itself.
- **[Tolsey](https://github.com/voyagi/tolsey)** is a food safety log for small kitchens that you fill in by voice. Tell it "reach-in two is fine" and it asks for the number on the thermometer. [Try it in the browser](https://tolsey.taranity.com), nothing to install.
- **[Throughline](https://github.com/voyagi/throughline)** is a memory layer for incident response that you can audit. When a search can't run, it answers "unknown" instead of "no prior incidents".
- **[Blast Radar](https://github.com/voyagi/datahub-blast-radar)** ranks what a data change is about to break, using DataHub's lineage, and writes the verdict back into DataHub. There's a [2-minute demo](https://youtu.be/cS7aZmGJl9g).
- **[Back on Track](https://github.com/voyagi/back-on-track)** is an offline web app and a set of printable fridge magnets for older adults with low back pain, in English and Dutch. [Open the app](https://voyagi.github.io/back-on-track/).

## A fix that shipped elsewhere

[claude-glass](https://github.com/cadentdev/claude-glass) did not work on Windows at all. Backslash paths broke every internal link and `serve` refused every file. My fix in [#31](https://github.com/cadentdev/claude-glass/pull/31) went out in [v0.7.8](https://github.com/cadentdev/claude-glass/releases/tag/v0.7.8), credited in the release notes.

The rest is side projects and a few forks I keep around. [taranity.com](https://taranity.com) is the studio I run.
