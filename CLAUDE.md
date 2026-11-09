# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **German-language educational documentation project** — "Build Your Own AI" — a step-by-step tutorial teaching students with no IT background how to run a small language model (SmolLM via Ollama) on a Raspberry Pi Zero 2W. There is no source code to build, compile, or test. All content is Markdown + images + CAD files, plus teacher material.

Repository: `github.com/fabianpingel/build-your-own-ai` (renamed from `ASG`). It is one workshop of a small series of school workshops by Fabian Pingel; the series overview lives in the separate repo `fabianpingel/workshops` (GitHub Pages).

## Directory Layout

- `docs/` — student-facing chapters (addressed with "Du")
- `images/` — screenshots and figures, shared by `docs/` and the slides
- `cad/` — 3D-printable case files (3MF, STL)
- `lehrkraefte/` — material for whoever runs the workshop:
  - `lehrkraefte/folien/slides.html` — the presentation, the **single authoritative source** for slides. It references images as `../../images/...` and fonts as `fonts/...` (in `lehrkraefte/folien/fonts/`).
  - `lehrkraefte/folien/slides-overview.md` — reference/correction document for the slides; may lag behind `slides.html`.
  - `lehrkraefte/firstboot_package/` — Bash/Python scripts for automatically setting up the classroom Raspberry Pis.

## No Build System

There are no build, lint, or test commands. This repository has no `package.json`, `Makefile`, `pyproject.toml`, or CI/CD configuration. Version control via Git is the only tooling in use.

## Content Language & Tone

All documentation is written in **German**, addressed informally to students using "Du" (not "Sie"). The writing style is encouraging and accessible — avoid technical jargon without explanation. Emoji are used intentionally throughout for visual structure and friendly tone (e.g., 🛠️ marks troubleshooting sections at the end of chapters).

## Chapter Structure

Chapters in `docs/` are numbered sequentially (`01_` through `10_`, plus `99_glossar.md`) and follow this internal pattern:
- Learning goal stated up front
- Step-by-step instructions with terminal commands in fenced bash blocks
- Screenshots referenced via relative paths to `images/<SubFolder>/`
- A **🛠️ Troubleshooting** section at the end

When editing or adding chapters, maintain this structure and the existing numbering convention.

## Image References

Images live under `images/` in named subfolders matching the chapter topic (e.g., `images/Ollama/`, `images/SSH/`). Reference them with relative paths from the `docs/` directory:

```markdown
![Alt text](../images/SubFolder/filename.png)
```

## Licensing

Documentation (`README.MD`, `docs/*.md`, author-created images): **CC BY-NC 4.0** — non-commercial use only, attribution required.  
Teacher material in `lehrkraefte/folien/` (except the font files): **CC BY-NC 4.0** as well.  
Code/scripts (e.g. `lehrkraefte/firstboot_package/`): **MIT License**.  
Third-party logos and brand assets are not covered by these licenses.

When adding content, ensure it respects these terms. Details are in `LICENSE.md`.
