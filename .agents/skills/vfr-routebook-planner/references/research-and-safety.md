# Research And Safety

Read this reference when route geography, airport facts, distances, current aviation details, or historical claims need external verification.

## Verification Scope

Before finalizing a routebook, verify as applicable:

- Airport name and identifier, field location, runway orientation, and nearby macro terrain or city context.
- User-selected waypoints, coordinates, leg distances, and ETE inputs.
- Macro visual features: coastlines, rivers, valleys, highways, railways, ridges, lakes, bays, urban edges, plains, and mountain walls.
- Each important feature's size, shape, relative position, surrounding context, and nearby lookalikes.
- Current non-weather aviation facts that materially affect the requested routebook, such as airport existence, airspace, procedures, restrictions, or navaids.
- Historical sites and commentary claims.

Do not browse merely to restate facts already supplied in reliable user route material. Do not fetch live weather unless the user explicitly requests it.

## Source Priority

1. User-provided Little Navmap plans, simulator flight plans, coordinates, charts, screenshots, or existing nav logs.
2. Official aviation and geography sources: AIP, FAA or local aviation authority material, official airport pages, government geospatial sources, and official charts.
3. Official or reputable history and tourism sources: museums, municipal or prefectural tourism sites, and cultural-heritage databases.
4. Reputable map and reference sources: OpenStreetMap, topographic maps, major map services, and established geography references.

Use map geometry rather than prose alone for cockpit-visible relationships. Cross-check a source when it establishes a name but not the visual position, scale, or shape needed for navigation.

## Calculations And Uncertainty

- Calculate leg distance consistently from the supplied plan or waypoint coordinates.
- Use `ETE minutes = distance_nm / ground_speed_kt * 60` and round only after calculating.
- Explain when the total excludes departure, climb, sightseeing orbits, holding, rerouting, and approach.
- If authoritative verification is unavailable, label the routebook as a draft and mark the specific uncertain legs or facts.
- Never convert a plausible map inference into a precise aviation claim without support.

## Real-World Boundary

For simulator routebooks, a concise disclaimer is sufficient. For real-world requests, state that the routebook does not replace current charts, NOTAMs, weather, airspace authorization, procedures, aircraft performance, or PIC and instructor judgment.

Do not create unsupported procedure-level guidance. Unless the user explicitly asks for it and current authoritative sources support it, end at visual airport-environment recognition and tell the pilot to use the applicable simulator or official procedure.
