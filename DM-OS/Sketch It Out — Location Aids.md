---
aliases: [Sketch It Out, Location Sketch Skill, sketch it out]
created: 2026-07-10T00:00:00.000Z
domain: DM-OS
source: [conversation 2026-07 (mill-grounds read-aloud + Gemini prompt process), campaign art references (cover + 3 environment plates)]
status: canonical
tags: [embers, dm-os, skill, process, visual-aids, art, read-aloud]
title: Sketch It Out — Location Aids
type: skill
visibility: dm-only
---

# Sketch It Out — Location Aids

Up: [[DM-OS & Prep]]

**A repeatable process for turning a campaign location into two player-facing aids: an in-game read-aloud that helps players *orient*, and a matched image prompt in the campaign's locked art style. Serves the DM-OS keystone (every recurring process → a player-facing artifact).**

> [!tip] Trigger
> This skill fires when I say **"sketch it out"** about a place — or close variants: *"sketch out [the location]," "give me a sketch of [place]," "let's sketch [place]."* When that happens for a **location**, run the workflow below instead of just free-writing.

## Scope
**For locations only** — dungeon rooms, shops, houses, streets, community/interior spaces, forest and outdoor areas, landmarks, the mill grounds, etc. **Not** for characters, monsters, items, or action beats (those may get their own skills later). If "sketch it out" is ambiguous about *what* place, ask which one before starting.

## What it produces (two artifacts, in this order)
1. A **player-facing read-aloud** describing the place at the table.
2. A **Gemini image prompt** in the locked house style (below).

Both are player-facing aids. *This skill note itself is DM-only.*

## Workflow

**Step 0 — Pull canon first.** If the location already has a vault note (or is described inside one — e.g. [[The Mill]], a delve-room note, an NPC's shop), read it and build on its real geography: layout, entrances/exits, adjacent features, scale, era details. Don't invent geometry that contradicts canon. If the place is brand-new, sketch the geography *with me* (or from a rough map I give you) before describing — see the mill-grounds map precedent.

**Step 1 — Write the read-aloud, then confirm.** Follow the description rules below. End with a compact **orientation key** and check it matches how I'm picturing the space **before** touching the image prompt. Do not generate the prompt until the layout is agreed — the whole point of Step 1 is that we're both seeing the same room.

**Step 2 — Build the image prompt** from the agreed description, using the locked art-style block verbatim and filling the per-scene variables. Offer the reference-image tip.

## Description rules (Step 1)
- **Orientation first, atmosphere second.** The read-aloud must let a player build a *mental map* and make decisions: what's where, relative positions (ahead / left / right / behind, near / far, high / low), the fixed **landmark(s)**, the **exits and paths**, and a sense of **scale**. Then layer atmosphere and flourish on top. Give them details that help them navigate — not *just* mood.
- **Write it as in-game read-aloud:** second person ("you…"), present tense, addressed to the table.
- **Anchor directions to the players' vantage** — where they're standing, the way they came in, what they just did — rather than compass headings, unless a compass genuinely helps.
- Prefer a few **grounding sensory specifics** (a real object, a sound, a texture, one telling detail) over piles of generic adjectives.
- **Length:** readable aloud in one pass — a healthy paragraph for a normal room, up to a few short paragraphs for a big establishing vista.
- Close with an **Orientation key** (a short DM-facing bullet list: *vantage / ahead / left / right / behind / far / notable features / any DM-only notes*). This is both our alignment check and the blueprint the image prompt is built from.

## Locked art style (reusable — goes in every prompt, verbatim)
> modern full-color graphic-novel / comic-book illustration; clean, confident ink linework under loose, atmospheric painted rendering; muted cel-style coloring; a single strong dominant light source; deep atmospheric perspective; filmic haze and painterly texture; nostalgic 1980s–90s Amblin / *Stranger Things* / *Paper Girls* sensibility; grounded Rust-Belt Americana; muted, desaturated palette.

The style has two poles, both ours: the **cover** (crisp full-color comic linework) and the **environment plates** (quieter painterly single-light interiors/spaces). Location aids should sit in the blend — comic linework *under* painterly cinematic rendering. See the style bible at the bottom.

## Per-scene variables (fill fresh each time, from the orientation key)
- **Composition / what's where** — foreground → midground → background, plus left/right/above/below and the POV/vantage. **State open vs. enclosed explicitly** — image models default to narrow one-point "hallway/canyon" shots, so if the space is meant to read wide and open, say so and consider a slightly elevated vantage; if it's tight and close, say that too.
- **Lighting & palette** — time of day + a **single dominant light source** (and its direction) + the muted palette. Optionally **one** deliberate warm/uncanny accent (the "one warm note" rule — e.g. a faint ember-orange glow as a focal or wrongness beat). Never more than one accent, and drop it if it would fight a warm sky (two orange sources muddy the read).
- **Mood** — the emotional register (eerie / hushed / inviting / melancholy / charged…).
- **Framing** — usually wide 16:9 cinematic landscape; choose eye-level (intimate/enclosed) or slightly elevated (open sweep) to control how the space reads.

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
- Any **text, logos, titles, or on-screen words**.
- **Anachronisms** — the period is **summer 1996, small-town Rust-Belt Ohio**; no modern signage, phones, cars of the wrong era, etc.
- **Unwanted people or vehicles** unless the scene calls for them.
- *Scene-dependent:* working electric lights in an abandoned/powerless space; a "smashed / overgrown ruin" look when a place is abandoned-but-intact; a narrow "hallway/canyon" composition when the space should read open.

## Practice notes
- **Attach 1–2 existing campaign art pieces to Gemini as style references** — a reference locks palette + rendering far better than words alone. Use the **cover** for color/linework and the "figures dwarfed by a landmark" composition; use an **environment plate** for painterly single-light spaces and mood.
- Keep every new location aid consistent with the bible below so the whole set reads like one book.

## Style bible (the reference art to match)
1. **Cover** — full-color comic linework, muted cel coloring, dusk; kids seen from behind, small against the blast-furnace mill above the falls. *(color, linework, "dwarfed by the landmark" composition.)*
2. **The study / archive** — warm painterly interior, one window shaft of light, bookshelves, dust. *(single-source light, muted, atmospheric.)*
3. **The pillared hall (dungeon)** — cool blue, carved pillars, a shaft of light from above, mist on cracked flagstones. *(cold palette, painterly, top light.)*
4. **The community room** — warm sepia interior, folding chairs, coffee urn, motes in the window light. *(muted, single warm source, quiet.)*

Common denominators across all four: **painterly rendering, one dominant light source, a muted/desaturated palette, atmospheric haze, cinematic framing.**

## Links
[[DM-OS & Prep]] · [[DM-OS — Architectural Principles]] · [[The Mill]] · [[Session 1 — DM Screen]] · [[The Mercer Falls Underground|Player-Facing Series]]

## Source
Codified from the mill-grounds "turn from the gate" read-aloud + Gemini-prompt process, and the four reference art pieces (cover + three environment plates) — conversation, 2026-07.