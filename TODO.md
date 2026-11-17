# Mount Carmel Command Center — Outcome Checklist

- [ ] The top of the dashboard identifies Hendrik Schoeman and the KALCON / 5C Mount Carmel assignment.
  - Acceptance: the name appears at the top of the dashboard for easy identification and future feedback.

- [ ] The homepage contains a detailed risk register template tailored to a Mount Carmel data-center construction project.
  - Acceptance: the register includes risk ID, category, description, cause, consequence, probability, impact, score, response, owner, trigger, due date, status, evidence, and export capability.

- [ ] The page contains the 30, 60, and 90-day transition plan.
  - Acceptance: the plan is organized by first week, first 30 days, days 31–60, and days 61–90, with practical construction-management activities.

- [ ] The page contains the current-state brief and stakeholder interview questions.
  - Acceptance: verified facts, assumptions, immediate unknowns, and role-specific interview prompts are visible and clearly labeled.

- [ ] The homepage contains a dynamic estimated project timeline with a “WE ARE HERE” arrow.
  - Acceptance: dates recalculate from the current date and every assumed phase is labeled as an assumption unless verified by KALCON/5C.

- [ ] The homepage contains a live news section.
  - Acceptance: news cards identify what changed, source, date, and positive/negative/neutral project impact; a refresh/search action is available.

- [ ] The page contains important reference links.
  - Acceptance: signed offer email, KALCON/5C interview record, Mount Carmel project site, Pennsylvania executive order, local hearing report, and onboarding references are linked where available.

- [ ] The page uses navy blue, khaki, and yellow.
  - Acceptance: the palette is consistently applied across navigation, cards, status chips, timeline, controls, and annotation UI.

- [ ] The annotation button is draggable to a section.
  - Acceptance: releasing it on a section opens a popup with a free-text input and a dropdown containing Manus, Claude, ChatGPT, Cola, Muse, Gemini, and Copilot.

- [ ] Annotation notes persist locally.
  - Acceptance: submitted notes are stored in the browser, displayed in an annotation list, and can be copied/exported; no external AI submission happens without a future integration.

- [ ] The HTML is self-contained and easy to edit.
  - Acceptance: the primary deliverable is one readable HTML file with embedded CSS and JavaScript and no secret keys.

- [ ] The page is published to GitHub and Cloudflare Pages.
  - Acceptance: a GitHub repository and a Cloudflare Pages URL are returned if authentication and deployment succeed.

- [ ] The HTML is stored in Google Drive under `_hendrikos/dashboards`.
  - Acceptance: upload is completed if the Drive connector is authenticated; otherwise the exact access limitation is reported and the local artifact is preserved.
