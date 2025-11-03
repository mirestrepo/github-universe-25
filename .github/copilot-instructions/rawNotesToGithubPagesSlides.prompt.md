---
description: Convert GitHub Universe 2025 raw notes into Marp markdown slides and deploy to GitHub Pages with automated CI/CD
---

# Plan: Convert Raw Notes to GitHub Pages Slides

Transform `raw-notes.txt` conference notes into markdown slides using Marp framework and auto-deploy to GitHub Pages via GitHub Actions.

## Steps

1. **Convert notes to Marp markdown** — Create `slides.md` from `raw-notes.txt`, adding `---` slide separators between sections and frontmatter with theme/styling config

2. **Add Marp build configuration** — Create `package.json` with `@marp-team/marp-cli` dependency and build scripts for local development

3. **Set up GitHub Actions workflow** — Create `.github/workflows/deploy.yml` using `marp-team/marp-action` to build HTML slides and deploy to `gh-pages` branch on push

4. **Configure GitHub Pages** — Enable Pages in repository settings to serve from `gh-pages` branch (done via GitHub UI after first workflow run)

5. **Update README** — Add links to live slides URL and local development instructions

## Open Questions

1. **Slide granularity** — Keep all notes as one presentation, or split into separate decks per topic (Agent HQ, Copilot features, MCPs, etc.)?

2. **Theme preference** — Use default Marp theme, Gaia (GitHub-style), Uncover (modern), or custom styling?

3. **Deployment trigger** — Auto-deploy on every push to `main`, or require manual approval/tag-based releases?

## Implementation Details

### Technology Stack
- **Framework**: Marp (Markdown Presentation Ecosystem)
- **Build Tool**: @marp-team/marp-cli
- **CI/CD**: GitHub Actions with marp-team/marp-action
- **Hosting**: GitHub Pages (gh-pages branch)

### Justification for Marp
1. **Zero-config simplicity** - Works with pure markdown, minimal setup required
2. **GitHub Pages friendly** - Exports to static HTML that deploys directly
3. **Markdown-native** - Uses standard markdown with minimal special syntax (just `---` for slide breaks)
4. **GitHub Actions integration** - Official action for CI/CD pipeline
5. **Perfect for conference notes** - Designed for technical presentations
6. **Active maintenance** - Well-supported open-source project

### Current Workspace State
- Repository: `github-universe-25` (owner: mirestrepo, branch: main)
- Existing files: `raw-notes.txt`, `README.md`
- No existing build configuration or GitHub Pages setup
- Clean slate for implementation
