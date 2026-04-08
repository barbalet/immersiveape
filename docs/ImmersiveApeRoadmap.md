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
- Cycle 7 lifts the interpolated weather field into the sky: overhead cloud masses now derive from the same smoothed cloud samples as the terrain patch, so the sky reads as a coherent rounded system rather than a separate set of random billows.
- Cycle 8 turns the interpolated coast into a fuller shoreline system: terrain, shallow water, and a dedicated surf-break layer now share the same shoreline sampling, which darkens wet sand and lays rolling foam over the rounded beach edge instead of leaving the coast as a simple land-water boundary.
- Cycle 9 pulls time-of-day back down onto the sea: the renderer now adds a sun-or-moon reflection path over deeper water and darkens water and surf more convincingly under cloud cover, so the coast responds to the sky instead of only sitting beneath it.
- Cycle 10 lets the sky travel across the land: the same interpolated cloud field now drives moving daylight shadow across terrain and vegetation, with low-sun warmth preserved between shadow bands so the world reads as weather passing over a single connected scene.
- Cycle 11 starts the biome palette layer promised for the next roadmap band: coastal sand, meadow, scrub, forest, and stone now use more intentional terrain and vegetation palettes, so the procedural world reads as differentiated regions instead of a mostly uniform green-brown surface.
- Cycle 12 deepens that biome layer into form: the same coastal, meadow, scrub, forest, and stone regions now push different vegetation silhouettes and rock clustering, so the world separates by shape instead of only by color.
- Cycle 13 turns those biome forms into habitat patches: vegetation now follows low-frequency density bands, creating dune clusters, meadow flower pockets, scrub tufts, forest floor litter, and stony clearings so the procedural world reads as regions with internal structure rather than evenly scattered props.
- Cycle 14 softens the seams between those biome patches: terrain now picks up ecotone tinting near neighboring materials, and vegetation adds edge-specific growth so coast-to-meadow margins, meadow-to-forest edges, scrub bands, and rocky fringes read as transitions instead of hard switches.
- Cycle 15 turns time-of-day into a fuller atmospheric system: dawn, dusk, and night now drive horizon glow, celestial halo, richer fog tinting, and low-light water color shifts so the world feels lit by changing air as well as changing sky.
- Cycle 16 teaches the terrain to read as relief: the renderer now measures local slope, ridges, basins, and runoff so exposed high ground picks up warmer stony accents, low sheltered ground cools toward damp green, and vegetation density follows landform instead of only biome color.
- Cycle 17 turns that relief into visible geology: runoff bands now lay damp traces and pebble deposits through low basins while steeper exposed ground sheds small scree clusters, so the terrain reads as shaped by drainage and collapse rather than only painted by elevation.
- Cycle 18 lets weather settle onto that landform system: rain now darkens inland ground, fills sheltered basins with reflective puddle pools, and makes runoff corridors respond to current weather instead of reading as permanently dry marks.
- Cycle 19 gives that inland water a living surface: runoff traces now carry animated sheen drifting downslope while rain pools layer moving ripple bands, so recent weather reads as active motion instead of static wet decals.
- Cycle 20 gives that water a terrain fringe: runoff now fans fine sediment into low ground while puddles form muddy rims and wet sedge tufts, so rain reads as reshaping surface edges rather than only darkening or animating them.
- Cycle 21 lets that wet ground breathe into the air: strong runoff corridors and pooled basins now lift low drifting haze, especially in twilight or fresh rain, so the aftermath reads as humid atmosphere instead of only altered terrain.
- Cycle 22 lets the flora inherit clearer genetic identity: the renderer now derives a biome DNA profile from the selected ape and world seed, pushes canopy, understory, bloom, drift, and rock clustering with it, and layers extra meadow, scrub, forest, coast, and stone details so vegetation reads as lineage-shaped habitat instead of a generic prop pass.
- Future cycles should preserve the Swift-first app structure and only drop into C when the simulation core or low-level bridge genuinely benefits from it.
