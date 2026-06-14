---
title: Vault Setup & Conventions
type: meta
domain: Meta
status: canonical
visibility: mixed
tags: [embers, meta, obsidian, setup, conventions]
created: 2026-06-14
---

# Vault Setup & Conventions

How this campaign vault is built, and the rules to keep it consistent. Modeled on the Arachne second-brain vault so the same patterns — and eventually a similar MCP connector (see [[MCP Connector Handoff]]) — apply here.

## Opening the vault
Obsidian works on folders. Point it at the `MercerFalls/` folder with **Open folder as vault**. Everything is plain Markdown — portable and yours. The `.obsidian/` folder holds local config (plugins, graph, appearance).

## How linking works (the key idea)
`[[Wikilinks]]` resolve by **note name**, anywhere in the vault — folders are irrelevant to resolution. The folder layout is purely for human browsing; you can move notes between folders without breaking links. **Build with links first; use folders lightly.** Link by the note's exact title (e.g., `[[Wesley Crane]]`), or with a display alias (`[[Wesley Crane|Wesley]]`).

## Folder layout (organizational only)
- **(root)** — entry points: [[Embers of the Gathering Hollows — Overview]] (home) and the domain MOCs.
- **Lore/** — cosmology and hidden truth ([[Lore & Cosmology]]).
- **Locations/** — town and dungeon places ([[Mercer Falls — Setting]]).
- **NPCs/** — character dossiers ([[Cast & NPCs]]).
- **Factions/** — groups and cosmic forces ([[Factions & Groups]]).
- **Systems/** — table mechanics ([[Game Systems]]).
- **Plot/** — the bizarro plot and Act 1 structure ([[Plot & Structure]]).
- **Episodes/** — the session/episode catalog ([[Episodes]]).
- **Bestiary/** — monsters ([[Bestiary]]).
- **Player-Facing/** — material safe to show players ([[Player-Facing Materials]]).
- **DM-OS/** — the prep operating system ([[DM-OS & Prep]]).
- **Meta/** — this note, [[Source Documents]], [[MCP Connector Handoff]].
- **Templates/** — note skeletons.

## MOCs over folders
The navigation backbone is **Maps of Content** — index notes like [[Cast & NPCs]] that link out to their members and carry a Dataview auto-index. Start at [[Embers of the Gathering Hollows — Overview]] and follow links. This scales better than deep folders and matches how a wiki is actually traversed.

## Properties (frontmatter)
Every note opens with YAML properties Obsidian reads as **Properties**. The schema:

| Property | Values | Purpose |
|---|---|---|
| `title` | The note's display title | Matches the H1 and filename |
| `type` | `moc`, `lore`, `location`, `npc`, `faction`, `system`, `plot`, `episode`, `monster`, `player-facing`, `dm-os`, `meta`, `template` | What kind of note this is |
| `domain` | `Lore`, `Setting`, `Cast`, `Factions`, `Systems`, `Plot`, `Episodes`, `Bestiary`, `Player-Facing`, `DM-OS`, `Meta` | The MOC family this note belongs to (the Arachne `pillar` analogue; what Dataview auto-indexes group on) |
| `status` | `canonical` (locked-in), `provisional` (first-pass, subject to revision), `stub` (placeholder), `tbd` (awaiting PC creation / not yet designed) | Design maturity |
| `visibility` | `dm-only`, `player-facing`, `mixed` | **Spoiler gate.** What an LLM/player may see. The future connector filters on this. |
| `tags` | list; always includes `embers` | Cross-cutting retrieval |
| `aliases` | list (optional) | Alternate names so links/searches resolve (e.g., `Mercer Steel Works` → [[The Mill]]) |
| `source` | list (optional) | Origin doc(s) + section, e.g. `"campaign bible v0.4 §6"` — traceability back to [[Source Documents]] |
| `created` | ISO date | When the note was made |

Keep these consistent — they're what lets Dataview auto-generate indexes and what the connector filters on.

## Note conventions
- **A note is an atomic, linkable entity** — one NPC, location, faction, system, plot thread, episode, or piece of lore. If you're writing about two things, that's two notes that link to each other.
- **Summarize and link; don't duplicate.** Notes capture the canonical facts and the connections, then point to [[Source Documents]] (via the `source` property and a `## Source` line) for exhaustive long-form detail. This keeps notes tight and retrieval focused (and honors the DM-OS minimalism principle — see [[DM-OS — Architectural Principles]]).
- **Up-links.** Every note links *up* to its domain MOC on the second line (`Up: [[Cast & NPCs]]`) and *sideways* to related notes inline.
- **Naming.** Title Case, human-readable; the filename *is* the link target. Episodes are named `Episode N — Title`.
- **DM-secrets get flagged twice.** Set `visibility: dm-only` (or `mixed`) and wrap the secret passage in a callout:
  ```
  > [!danger] DM-only
  > Wesley is being consumed by the dungeon exactly as Mercer was. He does not know this yet.
  ```
  Player-safe notes use `visibility: player-facing` and avoid callouts.
- **Status honesty.** If the bible/town reference/bizarro plot marks something "provisional" or "TBD / locked after PC creation," reflect that in `status` and say so in the body. Don't invent specifics the source held loose.

## Plugins worth turning on
Core (Settings → Core plugins): **Backlinks**, **Outgoing links**, **Graph view**, **Properties**, **Templates** (all already enabled in `.obsidian/core-plugins.json`).

Community (Settings → Community plugins → Browse):
- **Dataview** — powers the `## Auto-index` query blocks in every MOC (live lists of notes by `domain`). Install this first; without it the auto-index blocks render as code.
- **Templater** — richer templates than core; works with the `Templates/` folder either way.

## Backup
All local Markdown — version it with **Git** or use **Obsidian Sync**. (This vault lives inside a Google Drive folder, so it already cloud-syncs.)

## Start here
1. Open the `MercerFalls/` folder as a vault.
2. Open [[Embers of the Gathering Hollows — Overview]] and read down.
3. Install Dataview; the MOC auto-index blocks will then populate automatically.
4. Fill stubs and `tbd` notes as design firms up — especially after PC creation (see [[Outstanding Design Questions]]).
