# Reference-specific instruction brief

Generate this brief after inspecting all supplied panels and before image generation.

```text
[REFERENCE-SPECIFIC INSTRUCTIONS]

Character / moment:
- [identity-neutral visual summary, action, emotion, scene, and source art style]

Canonical visual facts:
- Face and expression: [only observed facts]
- Hair / headwear: [color, length, strands, silhouette]
- Body and pose: [orientation, gesture, foreshortening, supported extent]
- Clothing / accessories: [observed garments, colors, seams, folds, props]
- Lighting / atmosphere: [key light, shadows, background facts that must survive]

REFERENCE ROLE ASSIGNMENT:
- Image 1: [primary / secondary; exact visual regions and attributes]
- Image 2: [primary / secondary; exact visual regions and attributes]
- Image N: [primary / secondary; exact visual regions and attributes]

Priority rules for this set:
- Pose and geometry: [which images / regions control]
- Facial identity: [which image / region controls]
- Clothing details: [which image / region may fill otherwise invisible detail]

Continuity map:
- [panel A boundary] -> [panel B boundary]: [hair / anatomy / garment / shadow connection]

Allowed inference:
- [only genuinely unseen transition areas]

Do not:
- [specific distortions or redesigns to avoid, e.g. do not straighten a kneeling pose]
```

Use a primary reference only for the attribute it visibly establishes. For example, a face close-up can control facial identity but cannot override clearly visible leg geometry in another panel.

For a typical five-image set, a useful starting assignment is: Image 1 face/head; Image 2 torso/arms; Image 3 hips/legs/feet; Image 4 clothing-only supplement; Image 5 face-only supplement. Replace this with the actual evidence whenever the panels differ.
