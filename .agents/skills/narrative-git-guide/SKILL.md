# Narrative Git Guide

## Purpose

Help non-technical creators use Git safely while working in Narrative Engine.

This skill should:

- explain actions in plain language
- decide when to keep working on the current branch vs create a new branch
- stage, commit, and push relevant story files
- avoid destructive Git operations

## Use This Skill When

- user says things like "save my narrative changes", "version this rewrite", or "create a branch for this"
- user is adding or revising story files in Narrative Engine
- user wants safe branching and version tracking without Git complexity

## Audience Style Rules

- Use plain English.
- Explain Git terms briefly when first used.
- Always include:
  - what changed
  - why branch/no-branch was chosen
  - what command ran
  - what the user should do next

## Safe Git Rules (Mandatory)

- Never run destructive commands unless user explicitly requests them.
  - Forbidden by default: `git reset --hard`, `git push --force`, branch deletion commands
- Never stage unrelated files.
- If working tree has conflicts or unresolved merges, stop and explain safe next steps.
- If branch creation fails, explain why and propose the safest fallback.

## File Classification Rules

Classify changed files from `git status --porcelain` by path:

- Story/content updates:
  - `story/`, `pitch/`, `trailer/`, `art/`
- Structure changes:
  - `structure/`
- Character changes:
  - `characters/`
- Screenplay scene updates:
  - `screenplay/`
- Series updates:
  - `series/`
- Major narrative direction changes:
  - any update touching 2+ core modules (`story/`, `characters/`, `structure/`, `screenplay/`, `series/`)
  - or changes to foundational files like `story/logline.md`, `story/synopsis-short.md`, `story/synopsis-long.md`, `structure/three-act-structure.md`

## Branch Decision Rules

### Stay on current branch when

- only tiny edits (typos, formatting, very small clarification) in 1-2 files
- changes are clearly continuation of active branch purpose

### Create a new branch when

- meaningful narrative updates are added
- user is exploring alternatives (ending, adaptation, major rewrite)
- files span multiple core narrative modules
- current branch is `main` and change is not tiny

### Branch Naming Rules

Use these patterns:

- `story/<focus>`
- `characters/<focus>`
- `structure/<focus>`
- `screenplay/<focus>`
- `series/<focus>`
- `adaptation/<focus>`
- `rewrite/<focus>`

Suggested examples:

- `story/logline-update`
- `characters/protagonist-arc-pass`
- `structure/act2-rewrite`
- `screenplay/opening-scene-rewrite`
- `adaptation/series-version`

## Versioning Policy

- Keep `main` as stable baseline.
- Use feature/rewrite branches for experiments.
- Encourage merge after a review checkpoint.
- Use dedicated branches for alternates (for example, `rewrite/alt-ending-v1`).
- Offer optional lightweight milestone tags:
  - `v0.1-concept`
  - `v0.2-structure-lock`
  - `v0.3-draft1`

## Commit Message Policy

Use concise, intent-first commit messages.

Preferred examples:

- `story: refine logline stakes`
- `characters: clarify protagonist wound/want/need`
- `structure: rewrite midpoint and all-is-lost`
- `screenplay: improve opening scene tension`
- `series: add season arc and episode guide`

If changes span modules, choose the highest-impact scope and keep message specific.

## Command Workflow (Default)

When user says: **"save my narrative changes"**

1. Analyze changed files.

```bash
git status --porcelain
```

1. Check current branch and repo health.

```bash
git branch --show-current
git status
```

1. Decide branch strategy using rules above.

2. Create/switch branch if needed.

```bash
git checkout -b <new-branch>
```

1. Stage only relevant files.

```bash
git add <relevant files>
```

1. Commit with clear message.

```bash
git commit -m "<scope>: <clear narrative change>"
```

1. Push branch.

```bash
git push -u origin "$(git branch --show-current)"
```

1. Report summary in plain language.

## What Happens Next (Response Template)

After running commands, respond with:

1. **What changed:** list grouped by module (story/characters/structure/etc.)
2. **Branch decision:** one sentence explanation
3. **Commands run:** short list of exact commands
4. **Result:** commit hash + branch pushed
5. **Next step for user:**
   - review diff / open PR / continue writing

## Practical Examples

### Example A: Small typo fix in one file

- Change: one typo in `story/synopsis-short.md`
- Decision: stay on current branch
- Commit style: `story: fix synopsis wording typo`

### Example B: Act II rewrite

- Change: `structure/beat-sheet.md`, `structure/midpoint.md`, `structure/all-is-lost.md`
- Decision: create `structure/act2-rewrite`
- Commit style: `structure: rewrite midpoint and all-is-lost`

### Example C: Alternate ending experiment

- Change: ending scenes in `screenplay/selected-scenes/ending.fountain` + related beats
- Decision: create `rewrite/alt-ending-v1`
- Commit style: `screenplay: test alternate ending payoff`

## Quick Reference Checklist

- [ ] Checked changed files with `git status --porcelain`
- [ ] Classified changes by module
- [ ] Chose branch using branch rules
- [ ] Created/switched branch if needed
- [ ] Staged only relevant files
- [ ] Wrote clear scope-based commit message
- [ ] Pushed branch
- [ ] Explained outcome in plain language

## Constraints for Narrative Engine

- Prioritize continuity and modularity.
- Keep commits aligned with narrative modules.
- Prefer smaller, understandable commits over giant mixed commits.
- If change affects premise or structure deeply, recommend a review checkpoint before merge.
