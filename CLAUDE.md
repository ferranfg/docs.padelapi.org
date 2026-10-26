# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the documentation site for [Padel API](https://padelapi.org), built with [Mintlify](https://mintlify.com). The site provides API documentation, guides, and integration instructions.

## Development Commands

```bash
# Install Mintlify CLI (first time only)
npm install -g mint

# Start local development server (http://localhost:3000)
mint dev

# Run on custom port
mint dev --port 3333

# Check for broken internal links
mint broken-links

# Update Mintlify CLI
mint update
```

Deployment is automatic via GitHub integration when pushing to the default branch.

## Architecture

- **Format**: MDX files (Markdown + JSX) with YAML frontmatter
- **Config**: `docs.json` defines navigation, theme, and site settings
- **Components**: Mintlify components (Note, Tip, Warning, Card, CardGroup, etc.)
- **Snippets**: Reusable MDX fragments in `/snippets/`

### Navigation Structure

Navigation is defined in `docs.json` with two main tabs:
- **Guides**: Getting started, customization, writing content, AI tools
- **API reference**: API introduction and endpoint examples

When adding new pages, update the navigation in `docs.json` to include them.

## Content Standards

### Frontmatter Requirements

Every MDX file must include:
```yaml
---
title: "Clear, descriptive page title"
description: "Concise summary for SEO/navigation"
icon: "optional-icon-name"
---
```

### Writing Guidelines

- Use second-person voice ("you")
- Include prerequisites at the start of procedural content
- Add language tags to all code blocks
- Use relative paths for internal links
- Match style and formatting of existing pages

## Git Workflow

- Never use `--no-verify` when committing
- Never skip or disable pre-commit hooks
- Create a new branch when no clear branch exists for changes
