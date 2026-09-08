# cursor-drawing-skills

Standalone **Cursor Agent Skills** pack for observational drawing, likeness face sketch, and kids photo coloring pages.

These five skills are **not** part of [cursor-user-skills](https://github.com/chouswei/cursor-user-skills). Keep this pack in its own clone. Do not merge it into `cursor-user-skills`, and do not treat that repo as the source of truth for drawing method.

## Skills

| Folder | Use when |
|--------|----------|
| [kids-photo-coloring-page](kids-photo-coloring-page/SKILL.md) | Printable kids coloring from photos; likeness face gate first; artist method, not photo filters |
| [likeness-face-sketch](likeness-face-sketch/SKILL.md) | Face from photos until likeness passes; forms first; bare head gate; hair later |
| [localized-feature-study](localized-feature-study/SKILL.md) | One feature fails (brows, eyes, nose, mouth, ear, hand); study sheet; re-apply; do not redraw the whole character |
| [photo-to-sketch-practice](photo-to-sketch-practice/SKILL.md) | Ladder photoshoot (large / mid / micro); layout -> structure -> clarify; interpret, do not mindlessly trace |
| [comic-construction-basics](comic-construction-basics/SKILL.md) | Storytelling focal point; forms before detail; multi-angle consistency; clean ink; pairs with the other observational skills |

Trigger routing for agents: [AGENTS.md](AGENTS.md).

## How to use

Cursor loads Agent Skills from project `.cursor/skills/` and from the user pack `~/.cursor/skills` (Windows: `%USERPROFILE%\.cursor\skills`). This repo is a **drawing pack**. You can run it **alongside** `cursor-user-skills`, or **instead of** dumping these folders into that other repo.

### Alongside cursor-user-skills (recommended)

Keep `~/.cursor/skills` as [cursor-user-skills](https://github.com/chouswei/cursor-user-skills). Put this pack where the drawing project can see it:

```bash
git clone https://github.com/chouswei/cursor-drawing-skills.git
# Option A -- project-local (this workspace only)
mkdir -p /path/to/drawing-project/.cursor/skills
cp -R cursor-drawing-skills/kids-photo-coloring-page \
      cursor-drawing-skills/likeness-face-sketch \
      cursor-drawing-skills/localized-feature-study \
      cursor-drawing-skills/photo-to-sketch-practice \
      cursor-drawing-skills/comic-construction-basics \
      /path/to/drawing-project/.cursor/skills/
# Option B -- extra user-skill folders next to the other pack
# (copy the five skill directories into ~/.cursor/skills/ without replacing that git repo)
```

Do **not** clone this repository *over* `~/.cursor/skills` if that path is already `cursor-user-skills`.

### Instead of dumping into ~/.cursor/skills

Use this clone as the only drawing skill source for a drawing workspace:

```bash
git clone https://github.com/chouswei/cursor-drawing-skills.git /path/to/drawing-project
# Open that folder in Cursor. Skills live at repo root: <id>/SKILL.md
# To load them as project skills:
mkdir -p /path/to/drawing-project/.cursor/skills
ln -s ../../kids-photo-coloring-page /path/to/drawing-project/.cursor/skills/kids-photo-coloring-page
ln -s ../../likeness-face-sketch /path/to/drawing-project/.cursor/skills/likeness-face-sketch
ln -s ../../localized-feature-study /path/to/drawing-project/.cursor/skills/localized-feature-study
ln -s ../../photo-to-sketch-practice /path/to/drawing-project/.cursor/skills/photo-to-sketch-practice
ln -s ../../comic-construction-basics /path/to/drawing-project/.cursor/skills/comic-construction-basics
```

Or copy the five folders into `.cursor/skills/` if you prefer copies over links.

You do **not** need to dump these skills into `cursor-user-skills` for them to work.

### Point the agent at a skill

Ask in plain language (coloring page, likeness, one failing feature, photo practice, comic construction). The agent should open the matching `SKILL.md` and follow it. Sibling skills use relative Markdown links, not `sand-workflow:` URIs.

## Maintain

- ASCII filenames and folder names.
- Edit locally, then commit and push this repo only.
- Do not commit secrets, `.env`, or reference photos you do not own.
