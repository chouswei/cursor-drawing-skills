# Drawing pack -- agent routing

**Audience:** Cursor agents. **Pack:** this repo only -- **not** [cursor-user-skills](https://github.com/chouswei/cursor-user-skills).

Match the user request in at most two passes. Open one `SKILL.md`. Do not browse every folder. Prefer ASCII. Link siblings with relative paths (`../<id>/SKILL.md`). Do not use `sand-workflow:` URIs.

## Trigger table

| Task | Triggers | Skill |
|------|----------|-------|
| Kids coloring from photos | coloring page, kids colouring, printable outline, photo to coloring, crayon regions | [kids-photo-coloring-page](kids-photo-coloring-page/SKILL.md) |
| Face likeness from photos | likeness, face sketch, look like them, recognition gate, bare head | [likeness-face-sketch](likeness-face-sketch/SKILL.md) |
| One feature fails | eyebrows, eyes, nose, mouth, ear, hand study, landmark wrong | [localized-feature-study](localized-feature-study/SKILL.md) |
| Observational photo practice | photoshoot ladder, large/mid/micro, layout structure clarify, observational sketch | [photo-to-sketch-practice](photo-to-sketch-practice/SKILL.md) |
| Comic / illustration construction | focal point, forms before detail, multi-angle consistency, clean ink, hair stages | [comic-construction-basics](comic-construction-basics/SKILL.md) |

## Chain (do not skip)

1. Weak photo read or "practice from refs" -> `photo-to-sketch-practice`.
2. Face must be recognized -> `likeness-face-sketch` (bare head before hair).
3. Named landmark still wrong -> `localized-feature-study` for that part only.
4. Printable kids page -> `kids-photo-coloring-page` **only after** face approval.
5. Construction / ink / storytelling gaps -> `comic-construction-basics`.

If two skills match, pick the earliest gate that has not passed (likeness before page assembly). If still unclear, ask the user.
