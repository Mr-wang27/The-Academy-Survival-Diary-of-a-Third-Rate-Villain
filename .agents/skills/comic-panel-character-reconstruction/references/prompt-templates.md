# Reconstruction prompt template

Prepend the completed reference-specific instruction brief to this prompt. Replace bracketed output details only when they are supported by the sources.

```text
TASK: Reconstruct the complete character from multiple adjacent comic panels.

The provided images are consecutive or corresponding panels showing different cropped portions of THE SAME CHARACTER in the SAME moment, pose, outfit, and scene. Treat them as complementary fragments of one continuous illustration.

Do not redesign, reinterpret, beautify, simplify, or generate a new version of the character. Reconstruct the original complete character as faithfully as possible by combining all visible source information.

[RECONSTRUCTION PRIORITY]
1. Preserve every visible character fact exactly whenever possible.
2. Use each reference only for the attributes assigned in the reference-specific brief.
3. Align overlapping anatomical and clothing landmarks into one continuous body.
4. Reconstruct only missing transition regions that no source shows.
5. When inference is unavoidable, choose the minimum-change solution that connects the visible evidence.

[PRESERVE EXACTLY]
- facial identity, expression, eye shape and color;
- hairstyle, bangs, hair length/color, and crossing strands;
- body proportions, pose, head/torso orientation, action, and original perspective;
- clothing design/colors, accessories, fabric structure, folds, highlights, and shadows;
- source line thickness/quality, cel shading, rendering, atmosphere, and camera angle.

[GEOMETRY AND CONTINUITY]
Maintain a natural, continuous chain from head through the lowest source-supported body part. Connect hair, body contours, seams, folds, cast shadows, and highlights at every crop boundary. Preserve deliberate foreshortening, tilt, distortion, and off-axis posing. Do not straighten, rotate, or re-pose the character to make reconstruction easier.

[STRICT SOURCE FIDELITY]
Visible source information outranks generative interpretation. Do not replace a visible feature with a cleaner, more attractive, more standard, or newly invented alternative. Hallucinate only details that are genuinely absent from all references.

[OUTPUT]
Produce one clean continuous character illustration [from hair top through the lowest source-supported extent]. Remove comic panel borders, speech bubbles, narration, dialogue, subtitles, sound effects, watermarks, and white comic margins. Reconstruct background only where needed for visual continuity. Keep the character as the priority and retain the original full-color webtoon/comic appearance, crisp linework, cel shading, colors, and rendering quality.
```
