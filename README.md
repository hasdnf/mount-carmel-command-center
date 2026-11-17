# Hendrik KALCON / 5C Mount Carmel Command Center

This is a self-contained static HTML dashboard for Hendrik Schoeman’s transition into the KALCON Sr. Construction Manager / Site Director role supporting 5C at Mount Carmel Township, Pennsylvania.

## Edit the page

Open `index.html` in a text editor. All content, styles, risk data, timeline assumptions, news cards, questions, and interaction logic are contained in that file. Search for `const phases`, `const risks`, `const news`, and `const tasks` to update the working data model.

The dashboard deliberately labels the Mount Carmel timeline as an estimated planning model. Replace the assumed dates with the approved baseline schedule, current data date, WBS, and package milestones when KALCON/5C provides them.

The annotation workflow is local-only. Notes are stored in the browser’s localStorage, not sent to Manus, Claude, ChatGPT, Cola, Muse, Gemini, or Copilot. The selected model is a routing label for future manual use. Use Export notes to copy notes to the clipboard.

## Local preview

From this folder:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080/`.

## Publish

The same `index.html` is intended for GitHub Pages, Cloudflare Pages, or another static host. Do not add secrets to the file. Sensitive KALCON/5C documents should remain in the approved company document system; the public dashboard only links to non-sensitive reference pages and the user’s Gmail record.

## Source notes

The initial external-news snapshot and source URLs are in `data/news-sources.md`. News is not a project-control record; verify changes with KALCON/5C before acting.
