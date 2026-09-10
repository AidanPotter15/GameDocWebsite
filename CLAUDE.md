# Salvage project

Solo game project. Currently at concept stage with a documentation site and an unbuilt prototype.

## The one question

Does spoilage pressure ever make the player want to push for one more stop when they know they should go home?

Nothing gets built unless it helps answer this. If a proposed change doesn't, it belongs in `decisions/index.html` under "deliberately not built yet."

## What's in this repo

| Path | Purpose |
|---|---|
| `index.html` | Status board. The one table kept current. |
| `pitch/index.html` | One-page pitch, written to be posted for critique. |
| `prototype/index.html` | Spec, interactive route planner, build checklist, run log. |
| `decisions/index.html` | Every settled decision with its reason. |
| `assets/site.css` | Shared styles. All pages link this. |

Plain static HTML for GitHub Pages. No Jekyll, no build step, no dependencies. Don't add a framework or a bundler.

Each page is an `index.html` inside its own folder, so URLs read `/pitch/` with no extension. A new page means a new folder. Links between pages are relative (`../decisions/`), which keeps the site working at both the project URL and the custom domain.

## The prototype (not yet written)

C#, console, text only. Not Unreal. It's inventory, timers, quantities and state.

Core model: a hold of 20 bulk with 6 of it cold, seven fixed locations with limited stock, perishables on a clock, fuel that competes with cargo for hold space, and a cooler that degrades with travel.

## Numbers that were verified

All 1,956 possible routes were enumerated. Three things were wrong in the first draft and are now fixed. Don't reintroduce them:

- **Cold life must sit near route length** (10–18h). At 90h nothing ever spoiled and the cooler mechanic was decorative.
- **Stock per location must be limited** (6–8 bulk). Unlimited take means one stop fills the hold and no second stop is worth making.
- **Best score by stop count should run roughly 50, 88, 97, 99.** That flattening curve is the whole design. If a change makes it linear, the change is wrong.

Before changing any item life, stock quantity, tank size or distance, re-check both the fuel feasibility and that score curve.

## Scope rules

These exist because the failure mode on this project is building the interesting thing instead of the uncertain thing.

Do not build, suggest, or scaffold:

- 3D, terrain, world generation, art of any kind
- Driving as an activity, or any repair minigame
- Combat, enemies, threats
- Crafting, cooking, NPCs, story
- Site exposure / radiation (good idea, deliberately deferred — four clocks is too many)
- Uncertainty about whether an item is really spoiled (deferred, tests a different question)

If asked for one of these, say it's on the deferred list and why before doing it.

## Writing style

All prose in this repo follows the no-AI-slop ruleset at github.com/AidanPotter15/no_ai_slop_writing_rules. Plain and direct. No hype, no throat-clearing, no em-dash asides, no "not X but Y" constructions.

## Working notes

- The site's checklist and run log use `localStorage`, so state is per browser and per device. Task tracking that needs to sync belongs in GitHub Issues, not in the site.
- `index.html` status table is the only thing that should change often. If a row sits unchanged for two weeks, that itself is the finding.
