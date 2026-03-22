# Narrative Engine

**Write stories like software.**

A modular, Git-based storytelling framework for building films, series, graphic novels, and story-driven games with structure, version control, screenplay support, and AI collaboration.

## Why This Exists
Most narrative projects still live in one large document that becomes hard to revise, share, and scale.

Narrative Engine treats storytelling like system design:
- break the project into modules
- version decisions over time
- keep continuity explicit
- collaborate with humans and AI without losing intent

The result is a production-ready structure that supports early ideation, rewrites, pitch development, and delivery.

## Core Ideas
- **Modular storytelling:** Separate story, characters, structure, screenplay, art, trailer, and pitch assets.
- **Versioned narrative design:** Track decisions and rewrites through Git history.
- **AI-friendly architecture:** Clear source-of-truth files enable safer, higher-quality AI assistance.
- **Production continuity:** Keep narrative logic, thematic intent, and visual identity synchronized.

## Supported Project Types
- Feature films
- Limited series
- Episodic series
- Graphic novels
- Story-driven games

## Repository Structure
```text
narrative-engine/
  story/        # premise, synopsis, themes, world, narrative rules
  characters/   # cast design, relationships, psychology
  structure/    # frameworks, beats, causal flow, set-payoff design
  screenplay/   # Fountain drafts and selected key scenes
  series/       # season and episode planning
  trailer/      # teaser/trailer messaging and AI video prompts
  art/          # visual style and concept prompts
  pitch/        # one-pager, comps, and deck outline
  templates/    # reusable templates for new projects
  examples/     # practical sample mini-projects
```

## Recommended Workflow
1. Define project premise in `story/logline.md` and `story/synopsis-short.md`.
2. Expand world, themes, and emotional logic in `story/`.
3. Design core cast in `characters/` with clear wound/want/need arcs.
4. Build structure in `structure/` (three-act, midpoint shift, setup/payoff).
5. Draft scenes in `screenplay/` using `.fountain` files.
6. Prepare outward-facing materials in `pitch/`, `trailer/`, and `art/`.
7. Track all meaningful narrative decisions in `CHANGELOG.md`.

## Suggested Branch Strategy
- `main`: stable narrative baseline.
- `story/*`: high-level concept and world changes.
- `character/*`: character-specific revisions.
- `structure/*`: plotting and beat architecture updates.
- `script/*`: screenplay scene or draft passes.
- `pitch/*`: one-pager/deck/comps refinement.

Example branch names:
- `story/theme-reframe`
- `structure/midpoint-reversal`
- `script/opening-rewrite`

## Suggested Commit Style
Use clear, imperative commit messages with scope.

Examples:
- `feat(structure): add midpoint shift and pinch point alignment`
- `refactor(characters): tighten antagonist motive chain`
- `docs(pitch): update one-pager for investor meeting`
- `fix(screenplay): resolve continuity in opening sequence`

## AI Collaboration
Narrative Engine is designed for AI-assisted workflows. Keep edits modular and grounded in source-of-truth files.

- Read `AI_COLLABORATION.md` before using assistants.
- Ask AI to modify only specific modules unless a full rewrite is requested.
- Require AI to preserve continuity and explain tradeoffs.
- Keep `CHANGELOG.md` updated after major narrative decisions.

## File Formats
- **Markdown (`.md`)**: planning, strategy, structure, worldbuilding, production docs.
- **Fountain (`.fountain`)**: screenplay drafting in plain text, compatible with many script tools.

## Who This Is For
- Screenwriters and writer-directors
- Showrunners and writers' rooms
- Graphic novel creators
- Narrative game designers
- Creative technologists and AI-assisted storytellers

## Start Here
1. Read [`PROJECT_BIBLE.md`](PROJECT_BIBLE.md).
2. Read [`STORY_TECHNIQUES.md`](STORY_TECHNIQUES.md).
3. Read [`AI_COLLABORATION.md`](AI_COLLABORATION.md).
4. Copy template files from `templates/` into your working modules.
5. Start with `story/logline.md` and commit your first concept baseline.

## Roadmap
See [`TODO.md`](TODO.md) for planned improvements, integrations, and expansion packs.

## Author
Created by Fernando Portal  
Website: [https://valhallasolutions.net](https://valhallasolutions.net)

## Support This Project
If Narrative Engine helps your work, you can support ongoing maintenance and improvements.

PayPal: `nando_408@hotmail.com`  
Website: [https://valhallasolutions.net](https://valhallasolutions.net)
