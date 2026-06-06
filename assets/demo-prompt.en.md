# README demo prompt (English) — "Scavenger Awakening"

> English rendering of the same 15s, single-take demo, tuned for international
> models (**Veo / Kling / Sora** — English prompts preferred). Written with this
> repo's own `/shortfilm-prompt` 5-stage method. Original work by jnMetaCode,
> **MIT**. No IP names, so Kling's banned-word filter won't trip.
>
> 中文 / Seedance 2.0 原版：[demo-prompt.md](./demo-prompt.md)

```
Core theme: realistic hard-surface mecha | atom-punk post-apocalyptic scavenger | dusk ruins | battle-damage aesthetic | green energy-core charge-up | no game-CG feel

[Character & setup]
Subject:  A retro atom-punk salvage robot, ~2m tall, body assembled from brass
          and matte military-green steel plates. The head is a single round
          amber-glass optical lens (NOT a human face) with one fine crack across
          the glass. Paint is heavily flaked, exposing bare metal underneath;
          aged oil seeps from the joint seams; the chest plate is covered in
          scratches and dents; an old unrepaired weld is split open on the left
          shoulder. Never perfectly flat.
Material: Matte military-green steel + oxidized brass couplings + worn leather
          straps. A dark-emerald crystal energy core is set in the center of the
          belt, currently dark and unlit.
Scene:    Post-apocalyptic city ruins at dusk. Collapsed concrete structures,
          rusted rebar, half-buried wrecks of old machinery. Warm-orange dying
          sunlight cuts through drifting dust; hot wind lifts fine sand and
          scraps of paper; a faint electrical crackle in the distance.

[Atmosphere & quality]
Visual base:   Anamorphic widescreen cinematic. Sony Venice camera paired with
               Canon K-35 series lenses.
Color & tone:  Dual tone of dusk warm-orange + ruin cool-grey. Low saturation,
               high contrast. Shadows compressed but detail retained. Slight
               edge softness, pronounced film grain.
Style core:    Heavy-industrial hard sci-fi + post-apocalyptic wasteland.
               Emphasis on the real physical feedback of metal, dust, and energy;
               the solemn, oppressive solitude of a lone machine waking alone in
               the ruins.
Sound: No score. Production audio only (hot wind, fine sand scraping, metal
       creak, low-frequency energy hum, distant electrical crackle).

[Camera rules]
Single take: One continuous take, no editing.
Angle: Open on a right-side 30-degree low-angle close-up of the chest/waist.
       As the charge-up begins, orbit very slowly to a level front-on view.
       Finally pull out to a full-body wide of the figure standing in the ruins.
Breathing: Handheld shot. Throughout, maintain an extremely subtle, breath-like
           camera float to enhance presence, with an occasional slight tremor as
           if disturbed by heat waves.

0-3s · Dormant
Action: The robot kneels on one knee in the rubble, head bowed, amber optical
        lens dark, hot wind brushing the flaked shoulder plate.
Camera: Extremely slow push-in, catching dust glinting off the metal surface.
VFX:    A very faint green glow ignites deep inside the belt crystal core (core
        micro-flicker only, no spill); the edges of the lens crack shimmer faintly.

3-6s · Ignition
Sound:  A low-frequency hum approaches from far off.
Action: Brass fingers slowly press the belt energy core; the crystal is
        compressed and cracks; emerald light-fractures spread along the chest
        centerline.
VFX:    The core splits along its centerline, releasing a 0.3s reactive pulse;
        surrounding fine sand is blown up into a ring of dust; the metal edges at
        the flaked paint are rimmed with green light.
Camera: A 0.1s reactive micro-tremor lands with the pulse.

6-9s · Tearing
Action: The robot pushes off the ground and slowly rises; oil strings out of the
        joints with the motion; the old left-shoulder weld splits further open.
VFX:    Emerald light-fluid spreads from the core across the body, hissing and
        steaming where it meets the aged oil; some old scratches re-light and
        flicker frame-by-frame like circuitry, a few units glitch-flickering
        erratically.
Camera: A slight sway-and-defocus from the force of rising, snapping back after 0.5s.

9-12s · Charging
Action: The robot stands fully upright; the amber optical lens abruptly lights a
        steady emerald green, the crack filled in with light.
VFX:    Hexagonal green lights ignite frame-by-frame across the chest and
        shoulder heat-vents at an uneven coverage rate; belt core, chest, and
        shoulder vents form a triangular glow relationship; heat waves disturb
        the surrounding dust.
Camera: Orbit very slowly to a level, front-on eye-line.

12-15s · Awake
Action: The robot slowly lifts its head toward the dying sun at the end of the
        ruins; the optical lens holds a low-frequency green pulse (once per
        second); a small non-glowing "glitch" patch remains at the left-shoulder crack.
Camera: Orbit to a right-side 30-degree high angle and pull back very slowly,
        revealing the machine standing alone in the ruins.
Ending: No dialogue, no flashy light burst. Just hot wind continuing to carry
        dust across the machine, the dying sun sinking into the ruined skyline,
        the energy core pulsing faintly in the dusk.
```

## How to reproduce · 怎么复现

1. Paste the prompt above into **Veo**, **Kling** ([klingai.com](https://klingai.com)),
   or **Sora**. English prompts are preferred (especially Veo).
2. Single-shot 15s is a gacha — roll it **5–10 times** and pick the best take.
3. For a model with a dedicated negative-prompt field, drop in the reusable
   prefab from [../templates/negative-prompts.md](../templates/negative-prompts.md).
4. Abstract FX (the green energy-liquid spreading) lands ~70% of the time; that's
   acceptable for a demo.
