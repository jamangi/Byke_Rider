# Byke Engine

A document-based guide for an AI writing Byke Rider. Give the pilot a scene and ask what Byke would do or say; receive two compatible renditions with different narrative viewpoints.

Start with [HOW_TO_USE.md](HOW_TO_USE.md). Read [DESIGN.md](DESIGN.md) for architecture, tradeoffs, and the Luna / Sol / Astra comparison.

## Runtime reading order

The pilot reads these on every fresh task, followed by the operator's scene. Links are a reading manifest, not proof their contents have been loaded.

1. [PILOT.md](PILOT.md) — operating procedure and final checks.
2. [Full character sheet](../characters/byke_rider/character_sheet.md) — established character canon.
3. [CONTEXT.md](modules/CONTEXT.md) — facts, knowledge, uncertainty, and continuity.
4. [PERSONA.md](modules/PERSONA.md) — what drives his choices.
5. [TONE.md](modules/TONE.md) — what his words sound like.
6. [TASKS.md](modules/TASKS.md) — concurrent aims and shifting priorities.
7. [FORMAT.md](modules/FORMAT.md) — provisional group format and narrative lenses.
8. [Paired examples](examples/PAIRED_POSTS.md) — read both examples on the first use; thereafter the one relevant to the scene.
9. [Accepted continuity](context/CONTINUITY.md) and the operator-selected scene, using the [scene template](context/SCENE_TEMPLATE.md).

Each module contains its own short examples. The paired examples demonstrate the synthesis. They are hypothetical, not events that happened to Byke.

## Maintenance

Only operator-accepted events enter the continuity record. New posts are proposals; the two renditions are alternatives for one event, not consecutive turns. Keep campaign records separate if you run multiple continuities. No campaign has been initialized here.

This is an ordinary folder in the existing Git repository, not a nested repository or submodule. It needs no API key or executable service. A pilot still needs access to the document contents. Use Git commits to track changes and GitHub to share them; [the evaluation pack](evals/CASES.md) helps assess changes without mistaking attractive prose for fidelity.
