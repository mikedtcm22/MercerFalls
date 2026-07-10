---
name: sketch-it-out
description: Use whenever the user asks to 'sketch it out', 'sketch that out', 'sketch out [a place]', or otherwise create a visual and/or narrative aid for a LOCATION in their tabletop RPG campaign — a dungeon room, shop, building, street, forest or outdoor area, landmark, etc. Includes casual phrasings like 'sounds good, can you sketch that out for me?' Produces a player-facing read-aloud description plus a matched image-generation prompt in a locked art style. Do NOT use for characters, monsters, items, or action scenes.
---

# Sketch It Out — Location Aids

Turn a campaign location into two player-facing aids: (1) an in-game read-aloud that helps players ORIENT themselves, and (2) a matched image-generation prompt in the campaign's locked art style. Setting: a tabletop campaign set in summer 1996, small-town Rust-Belt Ohio.

## When to use
Trigger on "sketch it out" / "sketch that out" / "sketch out [place]" / "give me a sketch of [place]" — including casual forms ("sounds good, can you sketch that out for me?") — when the subject is a LOCATION (dungeon room, shop, house, street, interior, forest/outdoor area, landmark). Not for characters, monsters, items, or action beats. If it's unclear which place is meant, ask before starting.

## What it produces (two artifacts, in this order)
1. A player-facing read-aloud describing the place at the table.
2. A Gemini/image-model prompt in the locked house style (below).

## Workflow

**Step 0 — Establish canon first.** If a campaign-vault or notes connector is available, read the location's existing note (and any note that describes it) and build on its real geography: layout, entrances/exits, adjacent features, scale, era. Do not invent geometry that contradicts established canon. If no connector is available, or the place is brand-new, ask the user for the known geography (or a rough map) before describing.

**Step 1 — Write the read-aloud, then CONFIRM.** Follow the description rules below and end with a compact orientation key. Check that the layout matches how the user is picturing the space BEFORE building the image prompt. Do not generate the prompt until the layout is agreed — the point of this step is that both parties see the same space.

**Step 2 — Build the image prompt** from the agreed description, using the locked art-style block verbatim and filling the per-scene variables. Offer the reference-image tip.

## Description rules (Step 1)
- Orientation first, atmosphere second. The read-aloud must let a player build a mental map and make decisions: what's where, relative positions (ahead / left / right / behind, near / far, high / low), the fixed landmark(s), the exits and paths, and a sense of scale. Then layer atmosphere and flourish. Give details that help them navigate — not just mood.
- Write it as in-game read-aloud: second person ("you…"), present tense, addressed to the table.
- Anchor directions to the players' vantage (where they stand, the way they came in, what they just did) rather than compass headings, unless a compass genuinely helps.
- Prefer a few grounding sensory specifics (a real object, a sound, a texture, one telling detail) over piles of generic adjectives.
- Length: readable aloud in one pass — a healthy paragraph for a normal room, up to a few short paragraphs for a big establishing vista.
- Close with an Orientation key: a short bullet list (vantage / ahead / left / right / behind / far / notable features / any GM-only notes). This is the alignment check and the blueprint for the image prompt.

## Locked art style (paste verbatim into every image prompt)
> modern full-color graphic-novel / comic-book illustration; clean, confident ink linework under loose, atmospheric painted rendering; muted cel-style coloring; a single strong dominant light source; deep atmospheric perspective; filmic haze and painterly texture; nostalgic 1980s–90s Amblin / Stranger Things / Paper Girls sensibility; grounded Rust-Belt Americana; muted, desaturated palette.

The style has two poles, both valid: crisp full-color comic linework (hero/cover art) and quieter painterly single-light environment plates. Location aids sit in the blend — comic linework under painterly cinematic rendering.

## Per-scene variables (fill fresh each time, from the orientation key)
- Composition / what's where — foreground → midground → background, plus left/right/above/below and the POV/vantage. State OPEN vs ENCLOSED explicitly — image models default to narrow one-point "hallway/canyon" shots, so if the space should read wide and open, say so and consider a slightly elevated vantage; if it's tight and close, say that too.
- Lighting & palette — time of day + a single dominant light source (and its direction) + the muted palette. Optionally ONE deliberate warm/uncanny accent (the "one warm note" rule — e.g. a faint ember-orange glow as a focal or wrongness beat). Never more than one accent, and drop it if it would fight a warm sky.
- Mood — the emotional register (eerie / hushed / inviting / melancholy / charged…).
- Framing — usually wide 16:9 cinematic landscape; choose eye-level (intimate/enclosed) or slightly elevated (open sweep) to control how the space reads.

## Prompt template (fill the [brackets])
```
A full-color graphic-novel establishing illustration — painterly and cinematic — of [LOCATION: what it is + era/condition], seen from [VANTAGE/POV: where the viewer stands and what they're looking toward].

COMPOSITION [state OPEN vs ENCLOSED; low or slightly-elevated eye-level]:
- Foreground: [...]
- Midground: [...]
- Background / focal landmark: [...]
- [left / right / above / below / far distance, as the layout needs]

LIGHTING & PALETTE: [time of day]; [single dominant light source + direction]; muted, desaturated palette of [colors]; [atmosphere: mist / haze / dust / damp]. [Optional — one warm/uncanny accent: a faint [color] glow at [place], the only warm note.]

MOOD: [emotional read].

ART STYLE: modern full-color graphic-novel / comic-book illustration; clean confident ink linework under loose, atmospheric painted rendering; muted cel-style coloring; a single strong dominant light source; deep atmospheric perspective; filmic haze and painterly texture; nostalgic 1980s–90s Amblin / Stranger Things / Paper Girls sensibility; grounded Rust-Belt Americana.

FRAMING: wide 16:9 cinematic landscape; [eye-level / slightly-elevated] vantage.

AVOID: any text, logos, titles, or words; anachronisms (the year is 1996, Rust-Belt Ohio); unwanted people or vehicles; [scene-specific avoids].
```

## Global avoids (always include, then add scene-specific ones)
- Any text, logos, titles, or on-screen words.
- Anachronisms — the period is summer 1996, small-town Rust-Belt Ohio; no modern signage, phones, or wrong-era vehicles.
- Unwanted people or vehicles unless the scene calls for them.
- Scene-dependent: working electric lights in an abandoned/powerless space; a "smashed / overgrown ruin" look when a place is abandoned-but-intact; a narrow "hallway/canyon" composition when the space should read open.

## Practice notes
- Attach 1–2 existing campaign art pieces to the image model as style references — a reference locks palette and rendering far better than words. Use a hero/cover piece for color/linework and a "figures dwarfed by a landmark" composition; use an environment plate for painterly single-light spaces and mood.
- Keep every new location aid consistent with the established art so the whole set reads like one book.
