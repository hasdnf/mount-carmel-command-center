# Mount Carmel Command Center Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a self-contained, editable HTML command-center for Hendrik’s KALCON/5C Mount Carmel data-center role, publish the same source to GitHub and Cloudflare Pages, and prepare it for Google Drive storage in `_hendrikos/dashboards`.

**Architecture:** One static HTML file with embedded CSS, data, and JavaScript so future editors can make changes without a build tool. The page uses client-side date calculations for the assumed project timeline, localStorage for annotations, source-linked news cards with a refresh/search action, and a structured risk register template with CSV export. No sensitive credentials or project documents are embedded.

**Tech Stack:** Semantic HTML5, CSS custom properties, vanilla JavaScript, browser localStorage, GitHub CLI, Cloudflare Pages Direct Upload/API, Google Drive via gws or browser fallback.

**Spec:** User request in conversation dated 2026-11-08.

## Global Constraints

- Use the name “Hendrik Schoeman” at the top of the dashboard for identification.
- Use navy blue, khaki, and yellow as the core palette.
- Include the 30/60/90-day plan, current-state brief, stakeholder interview questions, detailed risk register template, useful reference links, dynamic timeline with a “WE ARE HERE” marker, and live news section.
- Clearly label Mount Carmel timeline dates and project status as planning assumptions unless verified by KALCON/5C.
- Include an annotation button that can be dragged to a page section, opens a free-text popup, and asks for a routing model: Manus, Claude, ChatGPT, Cola, Muse, Gemini, or Copilot.
- Do not send annotations to external AI services automatically; save them locally with the selected route and provide a copy/export path.
- Store the editable HTML in Google Drive under `_hendrikos/dashboards` if authenticated access is available; otherwise retain an upload-ready artifact and report the access limitation.
- Publish the page to GitHub and Cloudflare Pages using free/static hosting paths.
- Keep the page mobile-friendly and editable by future contributors.

## Design Decisions

- Design Read: mission-control dashboard for an executive construction leader; authoritative, high signal, evidence-first, slightly field-worn rather than glossy.
- Visual movement: “field operations command board” with a khaki paper-like canvas, navy rails, yellow decision markers, and hard-edged data blocks.
- Core principles: evidence before opinion; visible status; calm urgency; operational density without clutter.
- Color palette: navy `#0d2238`, deep navy `#071521`, khaki `#d7c9a6`, paper `#f4f0e7`, signal yellow `#f2c94c`, warning red `#c84b4b`, green `#3b7d68`.
- Typography: system sans stack for reliability and zero external dependency; condensed label styling via letter spacing and uppercase; serif-like emphasis avoided for dense mobile readability.
- Spacing: 8px base unit, 12/16/24/32/48 scales.
- Radius: 2px–10px, mostly square cards to feel like a field board.
- Shadows: restrained 0 12px 32px rgba(7,21,33,.12), with yellow inset rules for priority items.
- Motion: 160–280ms ease-out; timeline marker pulses once on load; drawers and dialogs use short slide/fade transitions; respect `prefers-reduced-motion`.
- Signature elements: yellow “WE ARE HERE” arrow, khaki metadata strip, dark navy section bands with mono-style labels.
- Brand essence: “A practical transition cockpit for entering a live mission-critical build.” Personality: direct, disciplined, prepared.
- Voice: “Here is what is verified.” “If it has no owner and date, it is not under control.”

## Project Structure

- `index.html` — deployable self-contained site and editable data model.
- `README.md` — editing and publishing notes.
- `docs/superpowers/plans/2026-11-08-mount-carmel-command-center.md` — this plan.
- `TODO.md` — outcome checklist and evidence notes.
- `data/news-sources.md` — source notes used for the initial news snapshot.

## Implementation Tasks

### Task 1: Create source content and data model

- [ ] Create the single-page HTML shell with semantic regions and navigation.
- [ ] Add the role context, offer facts, current-state brief, assumptions, and source-linked documents.
- [ ] Add structured arrays for phases, risks, stakeholders, questions, preparation tasks, and news.

### Task 2: Build visual system and responsive layout

- [ ] Implement navy/khaki/yellow tokens, executive dashboard hierarchy, mobile breakpoints, tables that wrap, and print-friendly styles.
- [ ] Add dynamic date strip and project timeline with assumption labels.

### Task 3: Implement interactive modules

- [ ] Implement tabs/section navigation, risk-register row filters, CSV export, copy-to-clipboard, checklist persistence, expandable news cards, and timeline recalculation based on current date.
- [ ] Implement draggable annotation button/drop targets, popup text entry, AI route dropdown, localStorage persistence, and annotation export.

### Task 4: Add operational reference content

- [ ] Include detailed 30/60/90-day plan, first-week questions, risk register fields, safety/quality/commissioning controls, document links, and explicit “verify with KALCON/5C” flags.

### Task 5: Validate and package

- [ ] Run HTML syntax/structure checks and a local HTTP server smoke test.
- [ ] Confirm the HTML is self-contained and contains no secrets.
- [ ] Create README and source notes.

### Task 6: Publish

- [ ] Create or reuse a dedicated GitHub repository, commit the static site, and push it.
- [ ] Deploy the same folder to Cloudflare Pages via the available authenticated API/CLI.
- [ ] Attempt Google Drive upload to `_hendrikos/dashboards`; if connector authentication is not available, preserve the artifact and report the exact limitation.
