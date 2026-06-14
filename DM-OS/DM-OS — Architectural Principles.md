---
title: DM-OS — Architectural Principles
type: dm-os
domain: DM-OS
status: canonical
visibility: dm-only
aliases: [DM-OS Principles, The Ten Principles]
tags: [embers, dm-os, principles, operations]
source: ["(DM-OS Docs)/dm_os_principles.md"]
created: 2026-06-14
---

# DM-OS — Architectural Principles

Up: [[DM-OS & Prep]]

**The ten slow-moving principles behind the campaign's operating system — the "how we run it" layer that sits above the campaign architecture. Expected to hold across every version of the spec; the running implementation lives in [[DM-OS — v0.1 Specification]].**

The DM-OS is the system for prepping, running, capturing, and improving a long-form weekly campaign. These principles are deliberately stable; versioned details belong to the spec.

## The Ten Principles

1. **Campaign-as-a-Service, players as co-investors.** Borrowed from Finance-as-a-Service. The DM serves the players and re-earns authority each session through value delivery — but players aren't consumer "customers," they're **co-investors** with a real, asymmetric, bidirectional commitment. Player engagement is load-bearing infrastructure, not a retention problem for the DM to absorb.
2. **Every cyclical process produces a player artifact.** The keystone organizing principle. Each recurring DM process must generate a player-facing artifact that makes the work intrinsically motivating; a process without one silently dies by session 12. (Capture → dispatch; prep → cold open + session; Monday refresh → recap agenda; light consolidation → fan-podcast; heavy consolidation → "last we saw them" video.)
3. **Canonical / emergent split, with memory consolidation.** Two layers: slow human-authored **canonical** docs (bible, [[The Bizarro Plot]], char guide, NPC briefs) and fast AI-queryable **emergent** state from play. The bridge is **consolidation** — modeled on sleep: *selection, abstraction, integration*. Three-tier memory (working / episodic / canonical). Guards against over-canonization; most emergent state should age out.
4. **Tactical / strategic split, with awareness-tagging.** Player-visible info splits into HUD-prominent / look-up-able / DM-narrated. Strategic info stays DM-private ([[Wesley Crane]]'s progress, the Surfeit counter, the realization-arc phase). The primitive: **PC-awareness as a property of every state change** — pays off at the lost-day mechanic ([[Death, TPK, and the Lost Day]]), where a hollowed PC's visible state freezes while the world moves.
5. **Sliver-at-a-time, integrated MVP.** Build a v0 of the *whole* integrated system, then improve pieces. A clunky-but-complete system beats a polished partial one. Test for v0 readiness: does the whole pipeline run 4 sessions unbroken? When unsure, choose one tier below ideal.
6. **DM intent goes in live segments, not durable artifacts.** Recaps stay clean (what happened, in voice); forward-leaning emphasis goes in the live "previously on" segment, delivered at peak attention.
7. **Player-led recaps via DM-prepped agendas.** The Monday refresh produces a recap *agenda* (beat sheet, one starred beat); a player narrates it 60–90 seconds at session start. Default: the player with the most spotlight last session.
8. **Minimalism discipline: every field, every artifact, needs a use case.** Schemas start aggressively minimal and grow only on a real query. When in doubt, kill the field; kill the artifact; add back only when its absence causes named pain. (See also the town's "texture pool" deferral logic in [[Outstanding Design Questions]].)
9. **Capture is the linchpin.** The single point where the whole pipeline can fail invisibly. Within 30 minutes of session end, structured signal is captured. If capture fails, every downstream artifact silently corrupts — so it earns top priority and a recovery protocol.
10. **The DM-OS is meta-architecture.** The architecture *of the architecture*. The OS-side question is never "would this make the campaign better narratively?" but "would this make the campaign more likely to still be running, healthily, at session 16?" Operational sustainability, not narrative quality.

## Source
`(DM-OS Docs)/dm_os_principles.md`. Implementation: [[DM-OS — v0.1 Specification]]. Onboarding schedule: [[DM-OS — Pre-Campaign Timeline]]. Open items: [[Outstanding Design Questions]], [[Next Prep Targets]].
