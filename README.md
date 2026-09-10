# Salvage project

Working documentation for a solo game project. Concept stage. Nothing here is final.

A salvage game set in a fixed, hand-made, post-collapse world. Your base is a
machine you drive, and it doubles as the save file. Nothing resets between runs.
What beats you is what you are carrying going bad before you get anywhere with it.

Cargo spoils on a clock. Cold storage degrades as you use it. Fuel competes with
cargo for the same hold space. The skill the game asks for is judgment about what
to take and when to turn back, so a bad run costs you the hold rather than your
health.

## The question this exists to answer

Does spoilage pressure ever make the player want to push for one more stop when
they know they should go home?

Everything on the site is there to answer that. Nothing gets built until it has
an answer.

## The site

https://glitchhaven.online/

| Page | What it holds |
|---|---|
| `/` | Status board. Where each part of the project stands. The one table kept current. |
| `/pitch/` | The one page pitch, written to be posted somewhere people will pick holes in it. |
| `/prototype/` | Spec, interactive route planner, build checklist, run log. |
| `/decisions/` | What was settled, why, and what was deliberately left out. |

## Where it stands

The concept is settled. The pitch is written and unposted. The numbers have been
checked against all 1,956 possible routes. The prototype is not started.

The prototype will be C#, console, text only. It is inventory, timers, quantities
and state. It exists to answer the question above and does not need to be
anything more than that.

## The checklist and run log

Both live on the prototype page and save with `localStorage`, so their state is
per browser and per device. Phone and desktop will not match.

Anything that needs to survive a device change belongs in GitHub Issues in this
repo rather than on the site.

## Working on the site

Plain static HTML. No build step, no dependencies.

```
python3 -m http.server 8000
```

Then open http://localhost:8000. Use the server rather than opening the files
directly, since each page lives in its own folder.
