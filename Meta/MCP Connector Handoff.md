---
title: MCP Connector Handoff
type: meta
domain: Meta
status: canonical
visibility: dm-only
tags: [embers, meta, mcp, connector, llm]
created: 2026-06-14
---

# MCP Connector Handoff

Up: [[Embers of the Gathering Hollows — Overview]]

Design notes for the planned **Mercer Falls MCP connector** — the campaign analogue of the Arachne vault connector — so an LLM (Claude Code, a table-side assistant) can read and update this vault during prep and play. This note is the spec to hand Claude Code when you build it.

> [!danger] DM-only
> This vault contains the full DM-side cosmology and Wesley's plan. The connector **must** respect the `visibility` property so a player-facing surface never leaks `dm-only` content. Treat `visibility` as the access-control boundary, not a hint.

## Why this works
Every note is plain Markdown with a consistent YAML schema (see [[Vault Setup & Conventions]]). That schema is the connector's contract: `type`, `domain`, `status`, `visibility`, `tags`, `source`, plus `[[wikilinks]]` for the graph. Anything the connector needs to filter or traverse already lives in frontmatter or links.

## Tool surface (mirror the Arachne connector)
Recommended tools, matched to how the Arachne vault connector is shaped:

| Tool | Behavior |
|---|---|
| `get_map(name?)` | Return a MOC's body plus its resolved members (`{title, type, domain, visibility}`). No name → the home note [[Embers of the Gathering Hollows — Overview]]. Primary entry point. |
| `list_notes(domain?, type?, folder?, visibility?)` | List notes matching filters. Returns `{title, path, type, domain, status, visibility, tags}`. |
| `read_note(title|path)` | Return `{title, path, frontmatter, body, outgoing_links}`. Resolve by basename (Obsidian-style) or exact path. |
| `search_notes(query, limit?)` | Case-insensitive text match over title, tags, body. Returns `{title, path, snippet}`. |
| `get_backlinks(title)` | Every note whose body wikilinks to the target. |
| `upsert_note(path, body, frontmatter?, message?)` | Create/update a note and commit. Used to log session outcomes, promote prep, update dispositions, mark `tbd` → `canonical`. |

## Access control (the campaign-specific addition vs. Arachne)
Add a **visibility mode** to the connector (e.g., `mode: dm | player`):
- **dm** mode: full access to all notes.
- **player** mode: only `visibility: player-facing` notes are readable; `dm-only` and `mixed` are excluded or returned with `dm-only` callout blocks stripped. This is what lets a player-facing "ask the lore" assistant exist without spoiling the campaign.

Implementation hint: filter on the `visibility` property at the `list_notes`/`search_notes`/`read_note` layer, and strip `> [!danger] DM-only` callout blocks from bodies in player mode.

## Update patterns the connector should support
- **Session logging.** After a session, `upsert_note` to the relevant [[Episodes]] note (what actually happened) and capture emergent canon (new NPC details, decisions) into the right dossier — the integrated counterpart to the [[DM-OS — v0.1 Specification|DM-OS capture loop]].
- **Disposition updates.** The Rivals' disposition tracks (see [[The Disposition Tracker]]) live DM-side; the connector can update each Rival note's frontmatter (e.g., a `disposition` field) as play moves the dial.
- **Promotion.** When a `tbd`/`provisional` note firms up (e.g., Sam's identity after PC creation — see [[Outstanding Design Questions]]), update `status` and fill the body.

## Boundary
Keep the connector's writes inside `MercerFalls/`. The long-form [[Source Documents]] in the parent folder are edited by hand; the connector operates on the integrated vault layer.
