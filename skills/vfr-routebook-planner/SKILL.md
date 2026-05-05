---
name: vfr-routebook-planner
description: Create Markdown VFR visual-flight routebooks and leg-by-leg navigation briefs for simulator or planning use. Use when the user asks Codex to make, revise, analyze, or format a VFR route book, route guide, flight sightseeing guide, companion navigator script, or Markdown nav log using headings, ETE, guiding lines, catch features, and scenery notes.
---

# VFR Routebook Planner

## Purpose

Create stable, leg-by-leg Markdown routebooks for VFR visual navigation. Treat each routebook as a practical companion navigator script: the pilot must be able to keep orientation from large, continuous terrain features before receiving scenery or history commentary.

Default to Chinese output unless the user asks for another language.

Use this skill for simulator flying, route planning, sightseeing nav logs, and Markdown route guides. Do not present the output as certified real-world flight instructions.

## User Defaults

Apply these defaults unless the user overrides them:

- **Aircraft**: Draco X.
- **Planning ground speed**: Use `120 kt` for Draco X simulator sightseeing routebooks when no speed is provided. If the user wants slower low-level sightseeing, use `100 kt`; if they provide an actual cruise/ground speed, use that value.
- **Output directory**: When creating a routebook file in this repository, save it under `navlogs/` by default, not `routebooks/`, unless the user explicitly requests another directory.
- **Route theme**: Prefer Japanese Sengoku-period history when planning scenic routes in Japan.
- **Historical emphasis**: When reasonable, route over or near castles, castle ruins, battlefields, old highways, castle towns, clan domains, and places associated with Sengoku figures.

## Core Principle

Build the routebook with a clear skeleton first, then add flesh.

- Skeleton: macro geography, heading, estimated time, continuous guiding line, and absolute catch feature.
- Flesh: scenery, history, local context, and visual highlights that enrich the flight after the navigation skeleton is clear.

Never rely only on small or ambiguous landmarks such as a single building, a small forest patch, a minor pond, or a vague compass bearing. Use them only as secondary confirmation.

## Airborne Landmark Disambiguation

Assume the pilot does not know local place names from the cockpit. A named city, river, lake, mountain, castle, road, or airport is not useful by itself unless the routebook explains how it looks from the air and how to distinguish it from nearby lookalikes.

For every primary guiding line, turn point, lake, river, valley, bay, mountain, or destination airport, describe its **visual signature**:

- **Scale**: say whether it is huge, medium, tiny, long, narrow, wide, basin-sized, bay-sized, etc. When helpful, include approximate length/width or compare it with nearby alternatives, for example `猪苗代湖是大型湖面，东西/南北尺度都很大，不是山北侧的小水库`.
- **Shape**: describe the outline visible from above: round lake, long narrow reservoir, hooked bay, straight coast, braided river, broad basin, mountain wall, saddle/pass, river confluence, delta, island chain, runway strip, etc.
- **Relative position**: anchor the feature to larger terrain: north/south/east/west side of a basin, at the foot of a mountain wall, on the coastal side of a ridge, the northern of two parallel rivers, the larger lake south of the small reservoir, the river that exits the wide plain, etc.
- **Context**: identify what surrounds it: sea on one side and mountains on the other, city grid on the plain edge, farmland around a river, volcano/mountain north of the lake, a bay mouth opening to the ocean, etc.
- **Lookalike rejection**: explicitly mention nearby confusing features and how not to choose them. If there are two similar rivers, lakes, reservoirs, valleys, coast inlets, or towns, write the differentiator in cockpit language: `take the northern/wider river`, `ignore the small reservoir north of the ridge`, `do not turn at the first small bay; wait for the broad bay with a city on its south shore`.

Do not assume the pilot can read place names on the terrain. Place names are labels for the routebook; airborne navigation must be possible from size, shape, direction, adjacency, and sequence.

## Inputs To Seek Or Infer

Before writing a full routebook, identify these values from the user request or the available context:

- Departure, destination, and intermediate waypoints.
- Aircraft or expected ground speed. Default to Draco X at `120 kt` for simulator routebooks if absent.
- Route purpose: efficient transfer, sightseeing, training, low-altitude VFR, mountain/coastal following, etc.
- Output scope: full routebook, one leg, revision, or critique.
- Desired region data source if the user provides one, such as Little Navmap, flight simulator waypoints, coordinates, charts, screenshots, or an existing plan.
- Historical theme preference. For Japan routes, assume Sengoku-period interest unless the user chooses another theme.

If key route geography is unknown and cannot be derived from provided material, say what is missing and avoid inventing exact local features. It is acceptable to draft a structure with placeholders.

## External Information Requirement

Before producing a final routebook, gather authoritative external information for airport and geography details unless the user has already provided reliable route data.

Do not fetch real-time weather by default. The user's simulator weather may differ from real-world weather, so omit METAR, TAF, winds, visibility, cloud base, and other live weather unless the user explicitly asks for them.

Confirm these items from authoritative or map-based sources:

- Airport names, ICAO/IATA identifiers, runway orientation, field location, and major nearby terrain or city context when relevant.
- Departure, destination, intermediate waypoints, coordinates, and distances needed for ETE calculations.
- Macro visual features: coastlines, rivers, valleys, highways, railways, ridges, lakes, urban edges, bays, plains, mountain walls, and other catch features, including their visible size, shape, nearby lookalikes, and relative position from the cockpit.
- Current non-weather aviation facts if they affect the routebook, such as airport existence, airspace, procedures, charted restrictions, or navaids.
- Historical sites and claims used in commentary, especially Sengoku-era castles, battles, clans, daimyo, roads, and castle towns.

Prefer sources in this order:

1. User-provided route material: Little Navmap plans, simulator flight plans, coordinates, screenshots, charts, or existing nav logs.
2. Official aviation and geography sources: AIP/FAA or local authority pages, official airport pages, government geospatial sources, official chart publications.
3. Official or reputable history/tourism sources: castle museums, municipal tourism pages, prefectural tourism pages, cultural heritage databases, museum pages.
4. Reputable map and reference sources: OpenStreetMap, topographic maps, major map services, encyclopedia/geography references.

If authoritative verification is unavailable, label the routebook as a draft and mark uncertain geography explicitly.

## Sengoku Route Preference

When planning routes in Japan, bias the route toward Sengoku-period interest as long as it does not weaken VFR readability too much.

Use Sengoku sites as route-shaping waypoints when they are close to a good visual corridor:

- Castle ruins and castle towns: mountain castles, flatland castles, reconstructed keeps, moats, old town grids.
- Battlefields and campaign routes: major engagements, sieges, clan borderlands, strategic passes, river crossings.
- Historic roads and valleys: Nakasendo, Tokaido, Hokuriku routes, Kiso Valley, mountain passes, coastal invasion or supply corridors.
- Associated figures: Oda Nobunaga, Toyotomi Hideyoshi, Tokugawa Ieyasu, Takeda Shingen, Uesugi Kenshin, Akechi Mitsuhide, Mori Motonari, Azai Nagamasa, Asakura Yoshikage, Sanada clan, and locally relevant daimyo.

Do not let historical routing break the navigation skeleton. If a historic point is visually small or hard to identify, treat it as a commentary point near a stronger visual anchor such as a river bend, castle town grid, mountain pass, lake shore, or coastline.

## Required Leg Formula

Every route leg must include these four elements:

1. **Heading/Bearing**: Give an approximate magnetic/true-style course or plain-language direction, such as `080° / 东北偏东`. Use it to establish the initial direction, not as the only navigation method.
2. **Time/ETE**: Estimate time from distance and ground speed. Default to Draco X at `120 kt`, approximately `2.0 NM/min`, for simulator routebooks when no speed is provided.
3. **Guiding Line**: Give a continuous visual feature that is hard to lose from the air, such as coastline, river, valley corridor, highway, railway, ridge line, lake shore, or urban edge. Include its visual signature: scale, shape, side-of-aircraft expectation, and surrounding terrain.
4. **Absolute Backstop / Catch Feature**: Give a large, unmistakable terrain or geography change that tells the pilot the leg is ending and a turn or new action is due, such as a coastline bend, mountain wall, bay mouth, broad plain, major river junction, large lake, or city edge. Explain why it is not the smaller or earlier similar feature nearby.

When a leg uses a named landmark that could be confused with another feature, add a **混淆排除** cue in either `引导线`, `终止点 / 兜底防线`, or `易错点`.

## Output Structure

Write Markdown routebooks with this order unless the user requests a different format:

```markdown
# [Route Name] VFR 路书

## 概览
- **用途**：
- **建议地速**：
- **总航程 / 总时间**：
- **导航策略**：
- **安全说明**：

## 航段 1：[Departure] -> [Waypoint/Destination]

### 主线导航 (Skeleton)
- **航向**：
- **预计时间**：
- **引导线**：
- **终止点 / 兜底防线**：
- **空中形态**：
- **混淆排除**：

### 历史与风景解说 (Flesh)
- **视觉彩蛋**：
- **战国史背景**：
- **相关人物**：

### 驾驶舱提示
- **确认点**：
- **易错点**：
- **下一动作**：
```

For short answers or single-leg work, use only the relevant sections.

## Style Rules

- Be concrete, spatial, and pilot-facing.
- Prefer large visible geography over named trivia.
- Describe landmarks as the pilot sees them from the air, not as map labels. Always give size, shape, relative position, and surrounding context for primary landmarks.
- If nearby lookalikes exist, name the cockpit-level difference before the pilot reaches them: bigger/smaller, northern/southern, first/second, coastal/inland, lake/reservoir, main river/tributary, broad basin/narrow valley, etc.
- For lakes and reservoirs, state whether the water body is huge, broad, long/narrow, dam-shaped, isolated, or attached to a basin. If a small reservoir or pond lies near the route, warn against mistaking it for the main lake.
- For rivers, specify which branch or parallel river to follow using relative position and behavior: northern/southern branch, wider main river, the one entering/exiting the basin, the river paired with the highway/railway, or the river that leads toward the visible mountain gap.
- For mountains and passes, describe the wall/gap/saddle shape and which side of the mountain mass the pilot should remain on.
- Use short paragraphs and bullets; routebooks should be scannable in flight.
- Put navigation before sightseeing in every leg.
- Use approximate phrasing when data is uncertain: `约`, `大致`, `可作为辅助确认`.
- Include calculations when useful, for example: `20 NM / 120 kt ≈ 10 分钟`.
- Keep scenery notes concise and subordinate to the guiding line.
- For Japan routebooks, make the historical commentary richer in Sengoku context: name the relevant clan, daimyo, battle, castle, or campaign, and explain why the terrain mattered.
- Keep historical commentary accurate and sourced; mark uncertain legends or disputed details as such.
- Make turn cues action-oriented: `到达这个兜底特征后，准备右转进入下一段`.

## Safety And Reliability Rules

- Do not fabricate exact headings, distances, airports, navaids, or terrain features when the route data is absent.
- Do not claim legal or operational authority for real-world flight.
- If the user appears to need real-world flight planning, recommend validating against current charts, NOTAMs, weather, airspace, aircraft performance, and instructor/PIC judgment.
- If using current airports, airspace, procedures, NOTAMs, charts, or regulations, verify with current authoritative sources before giving precise claims.
- Do not include real-time weather in simulator routebooks unless explicitly requested.
- If the route is for a simulator and the user provides simulator scenery or map context, optimize for what the simulator pilot can visually see.

## Quality Checklist

Before finalizing a routebook, verify:

- Each leg has heading, ETE, guiding line, and catch feature.
- The guiding line is continuous and visible at VFR scale.
- The catch feature is macro-scale and hard to overshoot unnoticed.
- Each primary landmark has an airborne visual signature: size, shape, relative position, and surrounding context.
- Any likely lookalike landmark has an explicit rejection cue, especially nearby lakes/reservoirs, river branches, parallel valleys, coastal bays, and similar towns.
- Turn points are described by terrain sequence as well as name: what appears before, what the target looks like, and what means the pilot has gone too far.
- For Japan routes, useful Sengoku sites have been considered and included when they fit the visual route.
- Historical figures, battles, and sites in the commentary have been checked against reputable sources or marked uncertain.
- Scenery/history does not obscure the navigation instructions.
- Any unknown geography or unverified data is labeled as uncertain.
- The Markdown is clean enough to paste directly into a routebook file.

## Revision Workflow

When revising an existing routebook:

1. Preserve useful route intent and user wording where possible.
2. Identify legs that depend on weak micro-landmarks.
3. Identify named landmarks that lack cockpit-visible description or could be confused with nearby similar features.
4. Replace weak cues with macro guiding lines, catch features, visual signatures, and lookalike rejection cues.
5. Recalculate ETE if distance or ground speed changes.
6. Return either the revised Markdown or a concise change list, depending on the user's request.
