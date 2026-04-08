# Immersive Ape Roadmap

Immersive Ape is being structured as a 100-cycle climb toward a playable demo, with each cycle intended to land a shippable increment rather than a speculative rewrite.

## Cycle Groups

- Cycles 1-10: Boot the full-screen Metal shell, connect it to ApeSDK state, establish the follow-camera, build the first terrain/ocean/weather rendering path, and make ape selection stable.
- Cycles 11-20: Replace placeholder meshes with robust procedural world generation driven by land genetics, location, tide, and weather fields. Land the first biome palette and stronger day/night transitions.
- Cycles 21-30: Expand flora generation into distinct coastal, grassland, bushland, and forest layers with DNA-aware variation and higher polygon fidelity.
- Cycles 31-40: Add richer ape body generation, locomotion, silhouettes, gait variation, and animation states for wandering, pausing, social proximity, and speaking.
- Cycles 41-50: Surface food seeking and foraging clearly in-world by rendering food classes, local abundance, search behavior, and outcome feedback around the selected ape.
- Cycles 51-60: Translate ApeSDK social systems into spatial storytelling with meeting behaviors, speech effects, memory traces, territory cues, and better visibility of friendships and conflicts.
- Cycles 61-70: Deepen sky, cloud, lighting, rain, fog, and surf rendering so that weather and time-of-day become major visual systems instead of simple overlays.
- Cycles 71-80: Improve interaction flow by introducing a proper ape-selection layer, lightweight camera control options, accessibility support, and the first floating-window mode.
- Cycles 81-90: Add audio, ambience, performance budgeting, LOD tuning, and stability work needed for longer sessions on Mac hardware.
- Cycles 91-100: Focus on demo readiness with polish, balance, onboarding, regression coverage, packaging, and a vertically complete “playable demo” pass.

## Current State

- Cycle 1 is the vertical slice foundation: a programmatic full-screen Metal app path, a renderer-facing ApeSDK snapshot bridge, a follow-the-selected-ape camera, and the first procedural environment pass.
- Cycle 2 deepens the readable demo slice: the immersive HUD now surfaces ape drives, goals, and state, while the renderer adds stronger rain, starfield, surf, and process-marking cues around food and nearby apes.
- Cycle 3 turns nearby ape activity into clearer spatial storytelling: the Mac HUD now carries encounter summaries and scene narration, the renderer draws social-contact ribbons for conversation/conflict/grooming/courtship, and the follow camera biases itself to keep important encounters readable.
- Cycle 4 moves the viewpoint closer to the selected ape itself: the immersive camera now uses state-aware embodied posture, and the renderer draws a foreground forelimb/chest layer so travel, feeding, swimming, conflict, and rest feel more like inhabiting the ape than observing it.
- Cycle 5 makes the selected ape's intent explicit: the renderer now picks a current attention target from food, nearby apes, courtship, conflict, or rest, draws a guide path and target marker into the world, and biases the follow camera and HUD toward that active focus.
- Cycle 6 softens the procedural world itself: terrain, coastline, beach, surf-edge, and cloud masking now interpolate between sampled points so landforms and weather fields read as curved transitions rather than blocky square steps.
- Future cycles should preserve the Swift-first app structure and only drop into C when the simulation core or low-level bridge genuinely benefits from it.
