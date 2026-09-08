---
name: kids-photo-coloring-page
description: >-
  Use when making a printable kids coloring page from real photos -- likeness
  face gate first, then assemble clean people-to-color line art (artist method,
  not photo filters).
---

# Kids photo coloring page (artist method)

Printable black-outline coloring sheet a child will recognize as a real person and scene. Observation from photos -- not edge-detect, not "photo to sketch" filters, not CV traces.

## When

- User wants a coloring page, kids colouring sheet, or crayon-friendly outline from family / personal photos.
- A likeness face already exists or must be produced first.

## MUST / MUST NOT

- MUST run [likeness-face-sketch](../likeness-face-sketch/SKILL.md) until recognition passes **before** assembling the full page.
- MUST keep the user's favorite composition if they named one (pose, crop, props).
- MUST deliver open black-and-white outlines with large crayon regions.
- MUST put the face as the storytelling focal point ([comic-construction-basics](../comic-construction-basics/SKILL.md)).
- MUST NOT use photo filters, auto-trace, or edge-detect dumps as the final page.
- MUST NOT assemble the full scene to "fix" a wrong face -- return to likeness / localized study.
- MUST NOT fill the final kids page with dense screentone unless the user asked.

## Pipeline

1. Collect refs. Prefer the user's photos. Ladder large / mid / micro per [photo-to-sketch-practice](../photo-to-sketch-practice/SKILL.md).
2. Character sketch + [likeness-face-sketch](../likeness-face-sketch/SKILL.md) until a viewer would recognize the person. Bare head gate, then hair. Closed mouth / thin low brows when the user or refs require it.
3. **Stop for face approval.** Do not layout the full coloring plate until the user accepts the face (or an explicit skip is given).
4. Assemble the page: readable silhouette, simplified props, character belonging in the scene. Keep named composition.
5. Clean ink pass over the underdrawing: open outlines, join gaps that would leak crayon, drop photo noise.
6. Title as hollow letters when a title is used.
7. Export Letter or A4 PNG, plus PDF when useful.

## Page craft

- Face / subject is the focal point; background supports, does not compete.
- Simplify clothing folds, furniture, and foliage into colorable shapes.
- One clear silhouette; avoid hair-thin inner noise.
- Props readable at arm's length for a child.

## Fail

Named landmark wrong (brows, eyes, nose, mouth, ear, hand) -> [localized-feature-study](../localized-feature-study/SKILL.md) on that part, then re-apply onto the approved construction. Do not redesign the whole page.

## Outputs

- Face-approval stills (from likeness) before the plate.
- Final kids page: Letter/A4 PNG (+ PDF). Open B/W outlines.

## Pair with

[likeness-face-sketch](../likeness-face-sketch/SKILL.md), [localized-feature-study](../localized-feature-study/SKILL.md), [photo-to-sketch-practice](../photo-to-sketch-practice/SKILL.md), [comic-construction-basics](../comic-construction-basics/SKILL.md).
