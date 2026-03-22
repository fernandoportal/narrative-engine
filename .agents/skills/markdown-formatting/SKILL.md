---
name: Markdown Formatting
description: Format and fix markdown files to avoid linting errors like MD022
---

# Formatting Markdown Files

When creating or editing markdown files in this project (e.g. character profiles, story scenes, project documentation), it is essential to follow standard markdown linting rules to maintain a uniform and clean structure.

## Core Rules to Remember

- **MD022**: Headings (e.g., `#`, `##`) must be surrounded by blank lines. Do not place text immediately under a heading without an empty line between them.
- Ensure consistent spacing between lists and paragraphs.
- Keep the narrative files easy to read in plain text.

## Validating and Fixing

You can fix formatting issues automatically by running the `markdownlint-cli2` tool. Whenever you create new narrative content, you may run this tool as a final step to ensure structural integrity across the repository.

```bash
npx -y markdownlint-cli2 --fix "**/*.md" "#node_modules"
```
