# Salvage project documentation

Working documentation for a salvage game prototype. Plain static HTML. No build step, no dependencies, no Jekyll.

## Publishing

These files sit at the repo root. To turn the site on:

Settings -> Pages -> Source: **Deploy from a branch** -> Branch `main`, folder `/ (root)`.

It goes live a minute or two later at https://aidanpotter15.github.io/GameDocWebsite/.

`.nojekyll` sits in the root so Pages serves the files as written and skips Jekyll processing.

## Local preview

Open `index.html` directly, or:

```
python3 -m http.server 8000
```

## Files

| File | Purpose |
|---|---|
| `index.html` | Status board. The one table to keep updated. |
| `pitch.html` | The one-page pitch, written to be posted for critique. |
| `prototype.html` | Spec, route planner, build checklist, run log. |
| `decisions.html` | What was decided and why. Read before re-arguing. |
| `assets/site.css` | Shared styles for all pages. |

## A note on the checklist and run log

They save with `localStorage`, which means per browser and per device. Phone and desktop won't match.

For anything that needs to survive a device change, use GitHub Issues in the same repo. It's free, syncs, sits next to the code, and does the job Trello was doing. Keep this site for documentation and keep tasks in Issues.
