---
title: Archivist AI Documentation
type: dm-os
domain: DM-OS
status: canonical
visibility: mixed
aliases: [Archivist AI, Archivist, myarchivist.ai]
tags: [embers, dm-os, tool, capture, reference]
source: ["(DM-OS Docs)/Archivist-AI-Documentation.md", "https://www.myarchivist.ai/documentation"]
created: 2026-06-14
---

# Archivist AI Documentation

Up: [[DM-OS & Prep]]

**A reference note on the third-party Archivist AI session-logging tool and how it slots into the campaign's capture loop. Archivist is the foundational platform for capture, episodic state, retrieval, and engagement analytics in [[DM-OS — v0.1 Specification]].**

> [!info] Visibility: mixed
> The tool's existence and player-facing features (Ask Archivist, the recaps, trading cards) are fine to share; the DM-private Journals holding [[The Bizarro Plot]] and cosmology are not. Permissions enforce the line.

## How Archivist Fits the Capture Loop

Archivist is the **linchpin** of the DM-OS pipeline (Principle 9 in [[DM-OS — Architectural Principles]]). It shifts capture from voice-memo + transcription to a Discord-integrated flow: `/start` opens a session, `/end` triggers automatic overnight processing, and the DM does a Session Review pass before the recap dispatch goes out. It also backs the look-up-able tier of player info via Ask Archivist.

## Getting Started

Create a campaign (name, description, system, language); add players (player name / character name / Discord handle); customize tone for recaps, the Ask Archivist chatbot, and image generation. 35+ languages supported.

## Adding a Session

Four ingestion paths: **Discord live record** (`/start`/`/end` — the campaign's primary path), **audio upload** (single-track only; many formats; transcription scales non-linearly with length), **play-by-post via Discord** (paste first/last message URLs), and **text upload** (transcript or raw notes, 750–5,000 tokens for raw notes). In-person tip: speak third-person to aid diarization.

## Working With Output

- **Session Review** — the editable pass over Archivist's output; edit Timeline (Steps are the backbone — edit first, then rerun the summary), curate Compendium and Moments, approve.
- **Timeline** — three-tier chronicle: **Major / Minor / Step** beats; auto-saves; feeds the summaries.
- **Quests** — campaign objective tracker (giver, objectives, progress log, success/failure conditions, related entities). Compile Quests from sessions via a diff drawer.
- **Compendium** — encyclopedia of Characters / Items / Locations / Factions; AI-generated descriptions are editable starting points; backstory is never AI-edited. Approve/reject/merge/reclassify new entities.
- **Moments** — notable session highlights; source material for the recap agenda.
- **Ask Archivist** — chatbot with recall of transcripts, summaries, entities, beats, lore; scoped by Journal visibility.
- **Tags** — `[[Entity Name]]` wikilinks between Characters/Items/Locations/Factions/Moments (color-coded; hover cards).
- **Data Studio** — network/relationship graph with session filtering and preset views; used in consolidation to spot dormant threads.
- **Session Handouts** — structured 2-page summaries (outline, key moments, encounters, highlights); pinned to `#handouts`. Not auto-saved — download.
- **Cast Analysis** — per-session engagement report (Talk Share donut, radar chart, speaker highlights, sentiment, AI Insights). Drives the consolidation engagement review.
- **Digital Trading Cards** — formatted entity cards (optional fun artifact).
- **Journals** — private/shared notes; **AI never edits them**; visibility (Private / Full party / per-user) controls both readership and whether Ask Archivist references them. Holds the canonical reference copy and DM-private strategic info.
- **Find & Replace** — preview-first rules to protect proper-noun spellings; standing rules apply to every new session.

## Admin & Discord

Roles: Owner / Admins / Regular Players (players see all published content + Ask Archivist, can't create sessions or see Session Reviews; can edit their own character). Campaign Cast improves speaker attribution. Action Hub centralizes high-frequency workflows. Discord integration provides voice-session recording, play-by-post ingestion, and Ask Archivist in Discord.

## Source
`(DM-OS Docs)/Archivist-AI-Documentation.md` (mirror of myarchivist.ai/documentation). Usage in the pipeline: [[DM-OS — v0.1 Specification]].
