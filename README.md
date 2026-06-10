# Script Bank

Your home base for short-form scripts. Write the scripts as files, see them all on one board.

## Open the board

Double-click **`index.html`**. That's it — no install, no server. (The old `dashboard.html`
still works, it just forwards you there.)

It's also live online, so you can check scripts from your phone anywhere:

**https://listya6.github.io/script-bank/**

Three ways to look at the same scripts:

- **Graph** — your five pillars sit in the middle, each script hangs off its pillar on a thin
  thread. The ring around a dot fills up as the script moves through the pipeline.
- **Board** — classic kanban columns: **Idea → Scripting → Shooting → Editing → Scheduled → Uploaded**
- **List** — a clean phone-friendly list, grouped by stage.

And on any script:

- **Full view** to read it fullscreen, distraction-free.
- **PDF / Print** to get a plain black-on-white A4 shoot sheet — just the hook, beat sheet,
  voiceover, on-screen text, B-roll and caption (the hook brainstorm and notes stay on
  screen). If it barely spills onto page two, the text shrinks a touch to fit one page.
- **Copy voiceover** to grab just the clean read for your teleprompter.

On a phone the screen stays clear — pillars, statuses, search and views all live behind the
hamburger menu.

There are soft click sounds on actions (open, close, filter, copy…) — Kenney's CC0
"Interface Sounds" pack, stored in `assets/sfx/`. The speaker button in the header (or the
hamburger menu on phone) mutes them; it remembers your choice.

## How you work with it (through Claude)

You don't hand-manage files. You just talk to Claude in this folder:

- *"New script idea: the geprek queue at 7pm as a traffic graph."* → Claude drafts it into the
  right pillar using `guidelines.md`.
- *"Move the studio booking one to shooting."* → Claude updates the status.
- *"I posted the SaraFun video, here's the link …"* → Claude marks it uploaded with the link.

After any change, Claude rebuilds the board's data automatically. Refresh the browser to see it.

## If you edit a file by hand

Change the top block of any script in `scripts/…` (e.g. `status: editing`), then run:

```
node build/build.mjs
```

…and refresh the browser. To update the online (phone) version too, commit and push —
GitHub Pages redeploys on every push.

## The important files

- **`guidelines.md`** — the rulebook for how a script gets written (your voice, structure,
  the numbers rule, how to end without sounding AI). Built from your 13 research notes.
- **`CLAUDE.md`** — how the system itself works (for Claude).
- **`scripts/`** — your actual scripts. The source of truth.
