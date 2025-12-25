<!-- .github/copilot-instructions.md - Guidance for AI coding agents -->

# Copilot Instructions — Landlord Guide Germany (static site)

Purpose: help AI coding agents be productive editing this small static website (HTML + CSS).

- **Big picture:** This repository is a single-page static site served via GitHub Pages. Major files:
  - `index.html` — single entry HTML page (site content and structure).
  - `style.css` — main styling; site uses plain CSS (no preprocessors or build step).
  - `README.md` — project description and deployment target (GitHub Pages).

- **Architecture & why:** No frameworks or server-side code — the site is simple, static, and intended for fast edits and GitHub Pages deployment. Keep changes minimal and focused on content + styles.

- **Local workflow / preview commands:**
  - Quick preview: open `index.html` in a browser (double-click or `open index.html`).
  - Serve locally (recommended for relative asset paths):
    ```bash
    # from repo root
    python3 -m http.server 8000
    # then open http://localhost:8000
    ```

- **Patterns & conventions to follow:**
  - Keep markup semantic and small — prefer plain HTML blocks inside `index.html` over adding JS.
  - Use existing CSS classes in `style.css`. When adding styles, append to `style.css` rather than creating new files unless asked.
  - No build/test tooling present — avoid introducing a build system without human approval.

- **Examples from this repo:**
  - To change header text, edit the relevant heading in `index.html` and adjust spacing in `style.css`.
  - To add a new resource section, copy the pattern used for existing sections in `index.html` to keep markup consistent.

- **Integration points & externals:**
  - Deployment target: GitHub Pages. No CI scripts detected. Do not assume Node, npm, or other toolchains are available.

- **When to create new files:**
  - Small content or style edits: modify `index.html` / `style.css` directly.
  - Add new assets under an `assets/` folder if adding images or downloads.
  - If a change requires a build tool or framework, leave a comment and create a PR for human review.

- **Commit & PR guidance for AI agents:**
  - Make minimal, focused commits with descriptive messages (e.g., "Update FAQ wording" or "Add rental checklist section").
  - For any structural change (new folders, toolchain), open a draft PR and describe rationale.

- **What NOT to do:**
  - Do not add or rely on package.json, webpack, or other build configs without approval.
  - Do not remove GitHub Pages–specific structure without checking deployment impact.

- **Where to look next:**
  - [index.html](index.html) — primary content and structure.
  - [style.css](style.css) — site styles.
  - [README.md](README.md) — project summary and intent.

If anything is unclear or you need more granular conventions (naming, branching, asset paths), ask and I'll iterate.
