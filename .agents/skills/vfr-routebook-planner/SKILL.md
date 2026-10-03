---
name: vfr-routebook-planner
description: Create or revise Chinese-first Markdown VFR sightseeing routebooks for flight simulators, with leg-by-leg headings, ETEs, visual guiding lines, catch features, cockpit disambiguation, and concise local history. Use for simulator VFR routebooks, route guides, navigation briefs, and nav-log reviews; do not use as certified real-world flight planning.
---

# VFR Routebook Planner

Create cockpit-readable visual-navigation routebooks for simulator or desktop planning. The pilot should be able to stay oriented from large, continuous terrain features before reading scenery or history commentary.

Default to Chinese unless the user requests another language. Never present the result as certified real-world flight instructions.

## Defaults

Apply these only when the user has not supplied a different value:

- Aircraft: Draco X.
- Planning ground speed: `120 kt` (`2.0 NM/min`). Use `100 kt` when the user explicitly wants slower low-level sightseeing.
- Route purpose: scenic simulator VFR rather than the shortest transfer.
- Japan theme: prefer useful Sengoku-period context.
- Repository output: when working in this repository, save new routebooks under `navlogs/` using the existing regional organization and a name such as `DEP-DEST-vfr-routebook.md`. Do not reorganize existing files.

## Determine The Task

Identify or reasonably infer:

- Departure, destination, and any required waypoints.
- Aircraft or planning ground speed.
- Efficient transfer, sightseeing, training, coastal, mountain, or low-altitude intent.
- Full routebook, one-leg draft, revision, analysis, or critique.
- User-provided route data such as a Little Navmap plan, coordinates, charts, screenshots, simulator waypoints, or an existing nav log.
- Desired historical or sightseeing theme.

Do not stop for details that the defaults safely resolve. If exact geography is missing and cannot be verified, produce only a clearly labeled draft or structure rather than inventing it.

## Workflow

1. Preserve the user's route, constraints, and requested format.
2. For a full routebook or substantive revision, read [references/routebook-method.md](references/routebook-method.md).
3. If the user has not supplied reliable route geography, airport facts, or distances, read [references/research-and-safety.md](references/research-and-safety.md) and verify them before finalizing.
4. For a Japan route or a requested Sengoku theme, read [references/japan-sengoku.md](references/japan-sengoku.md).
5. Build the navigation skeleton first: macro geography, course, distance/ETE, continuous guiding line, and unmistakable catch feature.
6. Add scenery and history only after every leg remains navigable without that commentary.
7. Recalculate totals from the leg data, run the quality checklist, and write the requested Markdown or concise review.

## Non-Negotiable Leg Contract

Every full routebook leg must provide:

- Approximate heading or plain-language direction.
- Distance and ETE based on the stated planning ground speed.
- A continuous visual guiding line at VFR scale.
- A large, unmistakable catch feature that marks the leg end or warns of overshoot.
- The primary landmarks' airborne visual signature: scale, shape, relative position, surrounding context, and any nearby lookalike rejection cue.
- A cockpit confirmation cue, common error, and next action.

A place name alone is never a navigation instruction. Prefer coastlines, broad rivers, valleys, highways, railways, ridges, lake shores, urban edges, bays, plains, and mountain walls over isolated buildings or small landscape details.

## Reliability Boundaries

- Do not fabricate precise headings, distances, airport data, navaids, procedures, or terrain features.
- Use approximate language for estimates and label uncertain geography.
- Do not fetch or include live weather for simulator routebooks unless the user asks; simulator conditions may differ from reality.
- For real-world use, tell the user to validate current charts, NOTAMs, weather, airspace, airport procedures, aircraft performance, and PIC or instructor judgment.
- Stop the visual routebook at airport-environment recognition unless the user supplies or explicitly requests procedure-level work based on current authoritative material.
