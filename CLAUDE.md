# portfolio

<!-- One paragraph: what this project is, who/what it's for, and its current phase.
     This file is auto-loaded every session — it is this project's durable system
     prompt. Keep it accurate; it is the first thing any agent (Claude or otherwise)
     reads. Everything above the managed block is yours to write. -->

## What this is

TODO: describe the project.

## How to work in it

- TODO: how to install / run / test (e.g. `make dev`, `pytest`, `docker compose up`).
- TODO: key conventions (style, branching, where things live).

<!-- BEGIN control-plane managed block -->
<!-- Managed by the control plane (~/control). Keep these markers; everything
     between them is kept in sync by `bin/control.py register`. Edit freely
     OUTSIDE the markers — that content is yours and is never touched. -->

## This project is managed by the control plane

It is registered in `~/control` and follows the shared persistence contract. You can
still work in it directly (`cd` here and `claude --resume`), but it is also
dispatchable from the control plane.

### Persistence contract (do this before you finish, every session)

Git is the spine: if it isn't committed and pushed, it can be lost. Before you stop:

1. Rewrite `docs/STATUS.md` to reflect the current state (it is a snapshot — overwrite it).
2. Append a dated entry to `docs/DECISIONS.md` for anything non-obvious you decided.
3. Tick / annotate any `docs/BACKLOG.md` items you worked on.

A `Stop` hook also commits + pushes automatically on every turn, so bytes survive
even if you forget — but the readable summaries above are your job.

### Not in git (must stay reconstructible)

Databases, docker volumes, and secrets are not committed. Keep migrations, seed
scripts, and `docker-compose.yml` in the repo so the environment rebuilds from
source. Secrets live in `.env` (git-ignored) and a password manager — never commit them.
<!-- END control-plane managed block -->

@docs/STATUS.md
@docs/BACKLOG.md
