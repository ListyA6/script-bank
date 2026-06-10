# CLAUDE.md — Script Bank operating rules

This repo is Listy's **script bank** for short-form video (Reels / TikTok / Shorts). Scripts
live as markdown files; `dashboard.html` is a kanban board that reads them.

## Two jobs in this repo

1. **Writing scripts** → follow `guidelines.md`. That's the rulebook (voice, structure,
   numbers rule, endings, ESL constraints). It's the distilled form of `researchnotes/`.
   Always read it before drafting a script.
2. **Managing the bank** → the rules below (schema, statuses, how to add/update, how the
   board stays in sync).

## Folder layout

```
index.html                double-click to open the board (works offline, no server)
dashboard.html            old entry point — just redirects to index.html
guidelines.md             the script-writing rulebook  ← read before writing
CLAUDE.md                 this file
scripts/<pillar>/*.md     the scripts (source of truth)
templates/script-template.md
data/scripts.js           AUTO-GENERATED index the board reads — never hand-edit
build/build.mjs           scans scripts/ → regenerates data/scripts.js
researchnotes/            the 13 deep-research notes (raw material for guidelines.md)
tests/                    scratch / eval output — not part of the bank
```

The board is also deployed at **https://listya6.github.io/script-bank/** via GitHub Pages
(repo `ListyA6/script-bank`, public). The site only updates on push.

## Frontmatter schema (every script starts with this)

```yaml
---
title:        # the working title (often the chosen hook line)
pillar:       # build-log | ops-floor | systems | failure | origin
status:       # idea | scripting | shooting | editing | scheduled | uploaded
platform:     # [reels, tiktok, shorts]
hook_type:    # receipts | build-reveal | contrarian | curiosity | pain-mirror |
              #   fail-story | bts | listicle | hot-take | before-after
length:       # 30s | 45s | 60s
created:      # YYYY-MM-DD
shoot_date:   # YYYY-MM-DD or empty
posted_date:  # YYYY-MM-DD or empty (fill when status -> uploaded)
link:         # post URL or empty
priority:     # high | normal | low   (high shows a dot on the card)
---
```

## Pillars (folders, by content angle)

| Pillar | What goes here |
|--------|----------------|
| `build-log` | shipping software, agency builds, dashboards, the actual code |
| `ops-floor` | restaurant ops, kitchen, staff, the physical moat |
| `systems` | how he systemizes a workflow; the operator-over-dev edge; teaching |
| `failure` | killed projects, losses, hard lessons |
| `origin` | backstory, the design-agency past, "X months in" honesty |

Pillars are just folders — rename/add/remove freely. Status is a **tag**, never a folder; a
file never moves between folders as it progresses.

## Statuses (kanban columns, left → right)

`idea → scripting → shooting → editing → scheduled → uploaded`

The board normalizes common synonyms (script→scripting, shoot→shooting, posted→uploaded,
waiting→scheduled, etc.). `uploaded` = done (card gets a ✓).

## Workflows

**Add a script:** copy `templates/script-template.md` into the right pillar folder, fill the
frontmatter + body per `guidelines.md`, then regenerate the index.

**Update status / any field:** edit the file's frontmatter (e.g. `status: editing`,
`posted_date: 2026-06-12`, `link: ...`), then regenerate the index.

**Regenerate the board's data (do this after ANY change under `scripts/`):**

```
node build/build.mjs
```

This rescans every `scripts/**/*.md` and rewrites `data/scripts.js`. The dashboard reads that
file, so the board only reflects changes after a rebuild + browser refresh.

> When Claude adds or edits a script, Claude runs `node build/build.mjs` in the same turn so
> the board never goes stale — then commits and pushes, so the phone version
> (GitHub Pages) stays fresh too.

## Conventions

- Filenames: short kebab-case, optionally date-prefixed (`2026-04-sarafun-closed.md`).
- The body follows the template sections (Hooks → Beat sheet → Voiceover → On-screen → B-roll
  → Proof shot → Caption → Notes). The dashboard renders all of it.
- `data/scripts.js` is generated. If it ever drifts from the files, just rebuild — the files
  win.
