# AI Collaboration Guide

Narrative Engine is optimized for human + AI narrative development. This guide defines how AI assistants should operate inside this repository.

## Core Operating Rules

1. Preserve continuity before adding novelty.
2. Make modular edits; do not rewrite the full project unless explicitly requested.
3. Keep narrative intent aligned with existing themes and emotional logic.
4. Record major narrative decisions in `CHANGELOG.md`.
5. Respect file-level authority and avoid contradiction.

## Authoritative Files (Source of Truth)

When conflicts appear, use this priority:

1. `story/logline.md` and `story/synopsis-short.md` for premise direction
2. `story/themes.md` and `story/emotional-logic.md` for thematic/psychological intent
3. `characters/` for motives, arcs, and relationship constraints
4. `structure/` for causal order and turning points
5. `screenplay/` for scene-level execution

AI should ask: “Does this edit preserve higher-level intent from authoritative files?”

## Preferred AI Editing Behavior

- Propose changes by module (`story`, `characters`, `structure`, `screenplay`)
- Explain tradeoffs when altering tone, pacing, or arc trajectory
- Keep names, timeline details, and world rules consistent
- Avoid introducing major lore or mechanics without updating `story/world.md` and `story/rules.md`
- Avoid introducing new character motivation without updating character files

## Continuity Checklist for AI

Before finalizing edits, validate:

- protagonist objective remains clear
- antagonist pressure remains active
- midpoint changes strategy or stakes
- setup/payoff links remain intact
- finale resolves core dramatic question
- theme expression is consistent across modules

## AI Assistance for Feature Films

AI should help with:

- beat diagnostics and pacing analysis
- scene objective clarity
- dialogue compression and subtext enhancement
- rewrite options that preserve act architecture

AI should avoid:

- flattening voice into generic language
- replacing character-driven turns with exposition

## AI Assistance for Series

AI should help with:

- season arc coherence
- episode differentiation and escalation
- continuity tracking across episodic threads
- B-story and ensemble balance

AI should avoid:

- resolving season-level conflict too early
- repeating episode conflict patterns without escalation

## AI Assistance for Adaptation (Film/Series/Graphic Novel)

When adapting formats, AI should:

- identify what must remain invariant (theme, core conflict, arc endpoint)
- redesign pacing and scene granularity for target medium
- update corresponding folders (`series/`, `screenplay/`, `structure/`) together

## Change Logging Protocol

AI should update `CHANGELOG.md` when a decision:

- changes premise, major stakes, or ending
- adds/removes primary characters
- shifts core thematic interpretation
- restructures acts or season architecture

## Prompting Best Practices

When requesting AI support, specify:

- module(s) to edit
- constraints to preserve
- desired output format (patch, rewrite, alternatives)
- acceptance criteria (tone, pacing, audience impact)

Example prompt:
> Revise `structure/midpoint.md` and `structure/scene-list.md` to strengthen causality after the midpoint. Preserve protagonist motivation and keep tone grounded thriller.

## Quality Standard for AI Contributions

A useful AI contribution should be:

- coherent with source-of-truth files
- concrete enough to implement immediately
- explicit about assumptions
- measurable in narrative effect (stakes, clarity, tension, payoff)
