# Routebook Method

Read this reference for a full routebook, a substantial rewrite, or a quality review.

## Skeleton Before Flesh

Build each leg in two layers:

- **Skeleton**: macro geography, heading, distance/ETE, continuous guiding line, catch feature, and next action.
- **Flesh**: scenery, history, local context, and visual highlights that enrich but never obscure the skeleton.

Do not rely on a single building, small forest patch, minor pond, or vague bearing as the primary cue. Use small landmarks only as secondary confirmation.

## Describe What The Pilot Sees

For every primary guiding line, turn point, lake, river, valley, bay, mountain, or destination airport, describe:

- **Scale**: huge, basin-sized, long and narrow, small, or an approximate size when useful.
- **Shape**: round lake, hooked bay, braided river, broad basin, mountain wall, saddle, delta, island chain, or runway strip.
- **Relative position**: north side of the basin, coastal side of the ridge, larger lake south of the reservoir, or river exiting the plain.
- **Context**: water on one side and mountains on the other, city grid at the plain edge, farmland around a river, or a bay opening to the ocean.
- **Lookalike rejection**: northern rather than southern river, second broad bay rather than first small inlet, main lake rather than nearby reservoir.
- **Sequence**: what appears before the target, what confirms it, and what proves the aircraft has gone too far.

The route must remain usable even when terrain labels are unavailable in the simulator.

## Required Leg Formula

1. **Heading**: approximate course plus plain-language direction. It establishes the initial direction but is not the sole navigation method.
2. **Distance / ETE**: state both when available. Calculate `minutes = distance_nm / ground_speed_kt * 60`; at `120 kt`, `ETE ≈ NM / 2`.
3. **Guiding line**: describe the continuous feature, its side of the aircraft, scale, shape, and surrounding terrain.
4. **Catch feature**: describe a macro-scale end marker or overshoot warning and explain why it is not an earlier similar feature.
5. **Cockpit action**: confirmation, likely error, and the next turn or navigation action.

If a named feature could be confused with another one, include an explicit `混淆排除` cue before the pilot reaches it.

## Full Routebook Shape

Adapt the labels to the region and theme, but keep navigation before commentary.

```markdown
# [Route Name] VFR 路书

## 概览
- **用途**：
- **建议地速**：
- **总航程 / 总时间**：
- **导航策略**：
- **风景 / 历史主题**：
- **安全说明**：

## 机场与资料核对
- **[Departure]**：
- **[Destination]**：
- **ETE 计算**：

## 航段 1：[Departure] -> [Waypoint/Destination]

### 主线导航 (Skeleton)
- **航向**：
- **距离 / 预计时间**：
- **引导线**：
- **终止点 / 兜底防线**：
- **空中形态**：
- **混淆排除**：

### 风景与历史解说 (Flesh)
- **视觉彩蛋**：
- **地方 / 历史背景**：
- **相关人物或景点**：

### 驾驶舱提示
- **确认点**：
- **易错点**：
- **下一动作**：

## 快速航段表

| 航段 | 路线 | 距离 | 航向 | ETE |
|---|---|---:|---:|---:|

## 资料来源
- [source links]
```

For a short answer or single-leg task, use only the relevant sections. Do not add empty ceremonial headings.

## Style

- Write concrete, spatial, pilot-facing instructions in short paragraphs and bullets.
- Use action-oriented turn cues: `到达这个兜底特征后，准备右转进入下一段`.
- State the expected side of the aircraft for a coastline, ridge, river, or lake shore.
- Distinguish rivers by branch, width, position, basin behavior, or pairing with a road or railway.
- Distinguish water bodies by size, outline, shoreline context, and whether they are coastal lagoons, reservoirs, or inland lakes.
- Describe passes as wall, gap, or saddle shapes and say which side of the mountain mass to remain on.
- Keep commentary concise near high-workload departure, turn, and arrival segments.
- Use `约`, `大致`, or `可作为辅助确认` for estimates.

## Revision Method

When revising an existing routebook:

1. Preserve sound route intent and useful user wording.
2. Find legs that rely on micro-landmarks, bare place names, or ambiguous bearings.
3. Replace weak cues with macro guiding lines, catch features, visual signatures, terrain sequences, and lookalike rejection cues.
4. Recalculate leg and total ETE when distance or ground speed changes.
5. Return revised Markdown or a concise change list according to the request.

## Quality Checklist

Before finalizing, confirm:

- Every leg satisfies the required leg formula.
- Guiding lines are continuous and visible at the planned VFR scale.
- Catch features are large enough that an overshoot should be obvious.
- Primary features include scale, shape, relative position, context, and useful lookalike rejection.
- Turn points include the terrain sequence before and after the turn.
- Totals agree with the leg table and the stated ground speed.
- Scenery and history do not bury navigation instructions.
- Unknown or unverified facts are labeled rather than invented.
- Markdown is scannable and directly usable as the requested artifact.
