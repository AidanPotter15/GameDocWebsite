# Salvage project documentation

Working documentation for a salvage game prototype. Plain static HTML. No build step, no dependencies, no Jekyll.

## Publishing

These files sit at the repo root. To turn the site on:

Settings -> Pages -> Source: **Deploy from a branch** -> Branch `main`, folder `/ (root)`.

It goes live a minute or two later at https://aidanpotter15.github.io/GameDocWebsite/.

`.nojekyll` sits in the root so Pages serves the files as written and skips Jekyll processing.

## Local preview

```
python3 -m http.server 8000
```

Then open http://localhost:8000. Use the server rather than opening the files
directly. Pages live in folders now, so a `file://` link to `pitch/` gives you a
directory listing instead of the page.

## Files

| File | URL | Purpose |
|---|---|---|
| `index.html` | `/` | Status board. The one table to keep updated. |
| `pitch/index.html` | `/pitch/` | The one-page pitch, written to be posted for critique. |
| `prototype/index.html` | `/prototype/` | Spec, route planner, build checklist, run log. |
| `decisions/index.html` | `/decisions/` | What was decided and why. Read before re-arguing. |
| `assets/site.css` | | Shared styles for all pages. |

Each page sits in its own folder as `index.html` so the URL has no `.html` on
the end. Adding a page means adding a folder, not a file.

## A note on the checklist and run log

They save with `localStorage`, which means per browser and per device. Phone and desktop won't match.

For anything that needs to survive a device change, use GitHub Issues in the same repo. It's free, syncs, sits next to the code, and does the job Trello was doing. Keep this site for documentation and keep tasks in Issues.
