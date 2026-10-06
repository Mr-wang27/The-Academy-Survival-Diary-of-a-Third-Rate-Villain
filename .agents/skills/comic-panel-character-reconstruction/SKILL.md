---
name: comic-panel-character-reconstruction
description: Reconstruct one continuous, faithful character illustration from two or more adjacent/corresponding comic or webtoon panels. Use when asked to merge cropped sequential panels, restore a complete comic character, or connect character fragments while preserving the exact original face, expression, pose, clothing, accessories, camera angle, atmosphere, line art, and cel shading.
---

# Comic Panel Character Reconstruction

Reconstruct the same drawing beyond its panel crops; do not redesign the character. Treat every input panel as complementary visual evidence from one scene.

## Required workflow

### 1. Inspect all evidence before generating

Read every supplied panel at useful detail. Do not start rendering after inspecting only the first image. Treat user-provided image names or notes as hints, but give visible image evidence priority.

Produce a **reference-specific instruction brief** for this set before constructing the image prompt. Keep it in the working response so the user can correct an incorrect reading. Use the format in [reference-brief-template.md](references/reference-brief-template.md).

The brief must state:

- the character and scene facts supported by the panels;
- each panel's role and priority for identity, pose, anatomy, clothing, or atmosphere;
- crop-boundary connections (hair, silhouette, fabric, shadows, hands, etc.);
- what is visible and therefore immutable, versus what is genuinely absent;
- any conflicts, ordered by visual evidence and then by the user's explicit role assignment.

Do not assume panel order or that Image 1 always shows the head. Infer roles from the images. If the user provides a role assignment, follow it unless it contradicts a plainly visible panel.

### 2. Assemble a constrained reconstruction prompt

Use the generic prompt in [prompt-templates.md](references/prompt-templates.md) plus the brief from step 1. Put the reference-specific brief before the generic prompt so the render has concrete evidence and a clear hierarchy.

Give source information priority over generative interpretation:

- Reproduce every visible feature rather than reimagining it.
- Infer only the smallest missing transition regions required to join fragments.
- Continue intersecting hair, contours, seams, folds, lighting, and shadows smoothly across crop boundaries.
- Preserve the actual camera, foreshortening, tilt, body action, expression, and mood. Never normalize an unusual leaning, kneeling, cropped, or action pose into a standing character.
- Remove panel borders, balloons, captions, sound effects, and margins from the result, but retain the character information they obscure only by minimal inference.

If the supplied images do not support a full body, render only through the lowest supported body extent; do not invent feet or other major anatomy merely to satisfy “full character.” State that limitation.

### 3. Generate and verify

Use the image-generation workflow with the inspected source images as references. If a renderer has a reference-image cap, still inspect every input image; select the smallest evidence set that covers face, pose geometry, clothing, and missing extremities, and encode the omitted panels' visual facts in the reference-specific brief.

After each result, compare it against every panel:

1. face, expression, eyes, hair, and head angle;
2. pose, perspective, crop-boundary alignment, and limb placement;
3. clothes, accessories, colors, folds, and lighting;
4. original linework, cel shading, environment, and emotional tone.

Correct only the mismatched evidence on the next pass. Never let a generated result replace the original panels as the identity source. Save versions with a new descriptive filename; never overwrite source panels.

## Conflict rules

Apply this order unless the user explicitly assigns a different one:

1. Direct visible detail in the panel covering that body region.
2. A user-specified primary reference for that attribute.
3. Overlapping geometry and continuity across adjacent panels.
4. Secondary references only for otherwise invisible details.
5. Minimum-change inference.

Never use a secondary clothing or face reference to replace a clearly visible pose-region detail in the primary panels.

## Deliverable

Return one clean, continuous character image in the source comic's rendering style. Preserve the scene's supported background only where it helps continuity; the character remains the priority. Report the evidence set used and any unsupported region intentionally left unreconstructed.
