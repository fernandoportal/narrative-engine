# Narrative Engine

**Write stories like software.**

A modular, Git-based storytelling framework for building films, series, graphic novels, and story-driven games with structure, version control, screenplay support, and AI collaboration.

## What if you could write films like code?

Narrative Engine helps you build stories using:

- modular files
- version control
- screenplay-ready structure
- AI collaboration

No more giant messy documents.  
No more lost story decisions.  
No more disconnected prompts.

## Quick Start (5 minutes)

1. Open `story/logline.md`
2. Write your story in one sentence
3. Define your protagonist in `characters/protagonist.md`
4. Build your beat sheet in `structure/beat-sheet.md`
5. Write your first scene in `screenplay/selected-scenes/opening.fountain`

You now have a working story system.

## 🧰 Recommended tools

### 🧠 Antigravity (recommended)

Use Antigravity as your main environment for Narrative Engine.

It is well-suited for:

- editing project files
- navigating the repository structure
- generating and refining story content
- working with AI using structured context from `story/`, `characters/`, `structure/`, and `screenplay/`

Antigravity acts as both your writing environment and your AI collaborator.

### 🧑‍💻 Visual Studio Code (optional)

Visual Studio Code is a strong optional setup if you prefer a traditional editor workflow.

Use it for:

- file management across modules
- Git workflows and branch handling
- editing Markdown and Fountain files

### 🔌 Recommended extensions

For VS Code users:

- **Better Fountain**
  - `.fountain` syntax support
  - screenplay preview
  - PDF export
  - scene structure visibility
- **markdownlint**
  - enforces consistent Markdown structure
  - improves readability
  - prevents formatting issues

### ⚡ Why this setup works

- Antigravity handles both writing and AI interaction.
- The repository provides the modular structure.
- VS Code extensions improve editing quality when you use VS Code.

This setup allows you to build stories modularly, maintain structure, and collaborate effectively with AI in a single workflow.

## How it works

`idea -> logline -> characters -> structure -> scenes -> screenplay -> iteration`

## Why Narrative Engine Is Different

Most writing tools are:

- linear
- document-based
- hard to version
- weak for AI context

Narrative Engine is:

- modular
- versioned
- AI-ready
- system-driven

## AI-First Storytelling

Narrative Engine is designed to work with AI in a structured way.

Instead of giving AI random prompts, you give it:

- story context
- character files
- structural logic
- scene targets

This leads to:

- better continuity
- stronger scene rewrites
- more useful AI collaboration
- less narrative drift

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

## In Use

This framework is designed for real creative development workflows, including:

- feature film ideation
- episodic series planning
- screenplay development
- AI-assisted story iteration

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

## Workflow Overview

1. Define project premise in `story/logline.md` and `story/synopsis-short.md`.
2. Expand world, themes, and emotional logic in `story/`.
3. Design core cast in `characters/` with clear wound/want/need arcs.
4. Build structure in `structure/` (three-act, midpoint shift, setup/payoff).
5. Draft scenes in `screenplay/` using `.fountain` files.
6. Prepare outward-facing materials in `pitch/`, `trailer/`, and `art/`.
7. Track all meaningful narrative decisions in `CHANGELOG.md`.

Featured example: `examples/full-film-mini/` (compact end-to-end workflow from premise to opening scene).

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
5. Explore `examples/full-film-mini/` for a compact end-to-end example from premise to scene.
6. Start with `story/logline.md` and commit your first concept baseline.

## How to Use Narrative Engine

Use this workflow to move from idea to production-ready draft with minimal confusion.

1. **Define your logline** in `story/logline.md`.
2. **Write short and long synopsis** in `story/synopsis-short.md` and `story/synopsis-long.md`.
3. **Build core characters** in `characters/protagonist.md`, `characters/antagonist.md`, and `characters/character-psychology.md` (wound, want, need, arc).
4. **Create the beat sheet** in `structure/beat-sheet.md`.
5. **Apply cause-and-effect logic** in `structure/but-therefore.md`.
6. **Define act structure** in `structure/three-act-structure.md` (or `structure/save-the-cat.md`).
7. **Create a scene list** in `structure/scene-list.md`.
8. **Write key scenes in Fountain** under `screenplay/selected-scenes/`.
9. **Assemble full screenplay drafts** in `screenplay/draft-v1.fountain` and `screenplay/draft-v2.fountain`.
10. **Iterate with intent**: revise structure first, then scenes, then dialogue polish.

Practical rule: if a scene is difficult to write, step back to `structure/` and verify objective, conflict, and consequence first.

## Recommended Workflow

Pipeline view:

`idea -> logline -> synopsis -> characters -> structure -> scenes -> screenplay -> iteration`

Use this sequence as your default. Skip steps only when you are intentionally doing exploratory writing.

## Versioning Your Story (Git Workflow)

Treat narrative decisions like software changes: explicit, reversible, and traceable.

### Suggested Branches

- `main` -> stable version
- `feature/rewrite-act-1`
- `feature/alt-ending`
- `feature/series-adaptation`
- `rewrite/dialogue-pass`

### Example Commands

```bash
git checkout -b feature/alt-ending
git commit -m "rewrite: improve emotional climax"
```

### Why Versioning Helps Story Development

- Explore alternate endings without destabilizing your main draft.
- Experiment safely with structure, tone, or format adaptations.
- Keep a reliable decision history for collaborators and future rewrites.

## Examples of Usage

A compact end-to-end example showing how to go from premise to scene is available in `examples/full-film-mini/`.

### Example 1: Film Project

- Define premise in `story/logline.md`.
- Build protagonist arc in `characters/protagonist.md`.
- Translate into structure using `structure/beat-sheet.md`.

### Example 2: Series Project

- Define season engine in `series/season-arc.md`.
- Break episode progression in `series/episode-guide.md`.
- Expand each episode in `series/episodes/episode-01.md` and beyond.

### Example 3: AI-Assisted Pass

- Feed AI your `story/synopsis-long.md`, `characters/`, and `structure/` files.
- Request a targeted improvement (for example, midpoint tension or scene clarity).
- Apply accepted changes module-by-module and log major decisions.

## Using AI with Narrative Engine

AI tools (ChatGPT, Codex, and similar assistants) work best when you provide focused context and clear boundaries.

### 1. Always Provide Context

At minimum, include:

- `story/synopsis-long.md`
- relevant files in `characters/`
- relevant files in `structure/`

### 2. Ask for Targeted Changes

Prefer requests like:

- improve a specific scene
- refine dialogue for one character
- expand one beat into scene options

### 3. Avoid Blind Full Rewrites

Do not ask AI to rewrite the entire project without constraints. Large blind rewrites usually break continuity, tone, and setup/payoff logic.

### 4. Example Prompt

```text
Read:
- story/synopsis-long.md
- characters/protagonist.md
- structure/beat-sheet.md

Now improve the opening scene with stronger emotional tension.
```

### 5. Use the Collaboration Standard

Follow [`AI_COLLABORATION.md`](AI_COLLABORATION.md) as the operating reference for continuity, authority files, and change protocol.

## Best Practices

- Build structure before writing the full screenplay.
- Keep files modular and purpose-specific.
- Use cause-and-effect logic (`BUT / THEREFORE`) to avoid episodic drift.
- Write scenes incrementally, then merge into full drafts.
- Use branches for experimentation and alternate versions.
- Maintain consistency across `story/`, `characters/`, `structure/`, and `screenplay/`.

## Roadmap

See [`TODO.md`](TODO.md) for planned improvements, integrations, and expansion packs.

## Author

Created by Fernando Portal  
Website: [https://valhallasolutions.net](https://valhallasolutions.net)

## Support This Project

If Narrative Engine helps your work, you can support ongoing maintenance and improvements.

PayPal: `nando_408@hotmail.com`  
Website: [https://valhallasolutions.net](https://valhallasolutions.net)
