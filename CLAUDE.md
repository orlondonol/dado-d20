# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository

Static HTML project hosted on GitHub Pages at **https://orlondonol.github.io/dado-d20/**

GitHub repo: `https://github.com/orlondonol/dado-d20` (public)

## Deploying

All changes pushed to `main` are automatically deployed via GitHub Pages. No build step required.

```bash
git add <file>
git commit -m "message"
git push
```

## Files

- `index.html` — D20 dice roller animation. Name input controls the result: `fernando/diego/luis/cesar/chilo` → 15–20, `papa` → always 1, anyone else → random 1–20.
- `personaje-papa.html` — RPG character sheet for "El Maestro Papá" (Yoda-Papa). All SVG artwork is inline, no external assets.

## Architecture

Pure HTML/CSS/JS — no frameworks, no build tools, no dependencies. All styles and scripts are inline within each `.html` file. External resource: Google Fonts CDN only.

## GitHub CLI

`gh` is installed and authenticated as `orlondonol`. Use it for repo operations:

```bash
gh repo create <name> --private
gh api repos/orlondonol/<repo>/pages -X POST --field 'source[branch]=main' --field 'source[path]=/'
```
