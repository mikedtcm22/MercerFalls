---
title: DM-OS — v0.1 Specification
type: dm-os
domain: DM-OS
status: provisional
visibility: dm-only
aliases: [DM-OS v0.1 Spec, v0.1 Specification]
tags: [embers, dm-os, spec, operations, archivist]
source: ["(DM-OS Docs)/dm_os_v0.1_spec.md"]
created: 2026-06-14
---

# DM-OS — v0.1 Specification

Up: [[DM-OS & Prep]]

**The first running version of the operating system, built on Discord + [[Archivist AI Documentation|Archivist AI]] + Avrae. Deliberately underbuilt: the integration test is whether the whole pipeline survives Sessions 1–4 unbroken. Implements the principles in [[DM-OS — Architectural Principles]].**

> [!note] Status: provisional
> This is v0.1 and is expected to be the most-revised DM-OS doc. Several components are "borrowed-from-platform" rather than fully designed.

## Operational Commitments (pre-Session 0)

- **Format** — episodic monster-of-the-week with a slow-burn [[Wesley Crane]] realization arc (modeled on *Buffy*, *Angel*, *Supernatural*). Episodic for resilience: one missing player doesn't break it.
- **Cast** — fixed 4 to start; 3-core + 1-recurring is an explicit fallback (architecture supports a core/recurring split).
- **Cancellation** — 3+ play normally; 2 = bottle-episode judgment call; 1 = cancel.
- **Schedule** — Tuesday 6:30–8:30pm CDT (1.5-hr session inside a 2-hr window).
- **Tech stack** — Discord (infra), Archivist AI (capture/state/retrieval/analytics), Avrae (mechanical HUD), Markdown (DM-side canonical truth), Zoom (backup).

## Cadence

| When | What |
|---|---|
| Tue 6:30–8:30 | Session (`/start` & `/end`) |
| Tue–Wed | Archivist auto-processes Session Review overnight |
| Wed–Thu | DM Session Review pass (30–45 min) + recap dispatch |
| Wed–Sun | Prep (~3 hr target, recalibrate after S3) |
| Sun eve | Recap agenda DM'd to next recapper |
| Mon | Light refresh + cold-open finalization |
| ~4 sessions | Light consolidation |
| ~16 sessions (per Act) | Heavy consolidation |

## Capture (the linchpin)

`/start`/`/end` in Discord triggers Archivist. Overnight it produces transcript, AI title, structured Timeline (Major/Minor/Step), summary, new Compendium entities, auto Moments, Cast Analysis. The DM's **Session Review pass** edits Timeline (Steps first), regenerates summary, curates Compendium and Moments, approves. **Recovery protocol:** if not done by Friday, do a 15-min minimal review to unblock; the pipeline tolerates one rushed review per ~4 sessions.

## State (three-tier)

- **Working memory** — the in-progress Session Review.
- **Episodic memory** — Archivist's Compendium / Timeline / Moments / Quest Log / Cast Analysis.
- **Canonical memory** — DM markdown (bible, [[The Bizarro Plot]], char guide, DM-OS docs) + a reference copy imported into Archivist **Journals (Private)** so Ask Archivist can ground answers. Archivist never owns canonical truth.
- **Threads** — a lightweight `threads.md` holds below-quest-tier story elements; quest-tier+ lives in Archivist's Quest Log. **NPC drift** is read as the diff between the bible brief and the Compendium entry.

## Distribution & Surfacing

- **Recap dispatch** (Wed/Thu) — ~250-word atmospheric "Mercer Falls Dispatch — Episode N" to `#in-character`; Archivist Session Handouts pinned to `#handouts`.
- **Recap agenda** (Sun) — 3–4 beats, one starred, DM'd to next recapper (default: most-spotlighted player).
- **Cold open** (finalized Mon) — DM-authored, 60–90 words, present tense, single image with one wrong beat, PCs not in scene; archived in `cold-opens.md`.
- **Info surfacing** — HUD-prominent → **Avrae**; look-up-able → **Ask Archivist** (permissions scope what players see); DM-narrated → the DM. Strategic info ([[Wesley's Sigils]] progress, the Surfeit counter, realization-arc phase, [[The Bizarro Plot]]) lives in DM-private Journals. Awareness-tagging is managed manually in Act 1 (coarse permissions only at the data layer).

## Consolidation

- **Light (~4 sessions, 60–90 min):** Cast Analysis review, Compendium scan, Quest Log compile, Data Studio dormant-thread scan, DM journal entry, optional bible promotion. **Artifact:** fan-podcast episode (first ships ~session 8; DM-authored, 600–800 words).
- **Heavy (per Act, ~session 16, 3–4 hr):** full Cast Analysis / Compendium audit / Timeline review / Data Studio scan / Quest close-out, **bible revision pass** (the major move), and pattern observations promoted to design principles. **Artifact:** "Last we saw them" Discord post (prose + image links + Spotify song; no video at v0.1).

## Open Questions for Session 1 Readiness

Closed: platform, audio capture, Archivist greenlight. Still open: the prep-budget number, the Session 0 onboarding flow doc, the Archivist tone-customization prompt, the Find & Replace rule list, and recap-dispatch voice calibration. (See also [[Outstanding Design Questions]].)

## Source
`(DM-OS Docs)/dm_os_v0.1_spec.md`. Principles: [[DM-OS — Architectural Principles]]. Tool reference: [[Archivist AI Documentation]]. Schedule: [[DM-OS — Pre-Campaign Timeline]].
