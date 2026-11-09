# Instructions for animation agents

The user wants a complete animated pet based on the exact individual dog in this repository.

1. Read `prompts/full-animation.zh-CN.txt`, `docs/animation-delivery.zh-CN.md` and `docs/identity-and-workflow.zh-CN.txt`; actually inspect the reference images in `assets/reference/` before generating.
2. Use `XH_REF_V1_PHOTO` as the canonical identity. The original photo and current turnaround sheets define appearance. The face sheet governs local face/ear detail; the sitting sheet governs pose. These are complementary views of one dog.
3. Preserve anatomical LEFT upright ear and RIGHT folded-tip ear. Front view: viewer-left folded, viewer-right upright. Back view: viewer-left upright, viewer-right folded. Never mirror a left/right animation to replace its opposite when doing so swaps identity.
4. Tail is a long, fluffy, black, low-carried plume, not a tight high curl. Keep the face, dark brown eyes, charcoal/cream fur mapping, gray-black muzzle, proportions and rendering style fixed.
5. `archive/legacy-v2/` is historical context only; its visuals differ and must not become identity references.
6. First create/review one character-correct keyframe, then one action at a time, then the coherent look-direction family. Do not ask an image/video generator to solve all actions as one scene or a large atlas in one step.
7. Keep input references fixed across jobs. Do not use a distorted generated frame as the sole reference for subsequent jobs. Head/gaze direction changes must not rotate the entire sprite.
8. Review beginning, middle and end frames and direction transitions. Fix drift, swapped ears, wrong coat patterns, broken anatomy, clipping, scale changes and bad loops before claiming completion. Prompt text alone is not evidence of consistency.
9. Put new assets and source/export metadata in `animations/`. Preserve the supplied reference images and their manifest. Record uncompleted actions honestly; do not fill missing animation rows by repeating static frames and call them finished.
10. Default deliverables are named PNG sequences, per-action motion previews, neutral/default image, an ordered 16-direction set, timing metadata and a QA report. Confirm actual target app requirements before claiming an atlas is import-ready.
