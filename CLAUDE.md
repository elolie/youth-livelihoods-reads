# Youth Livelihoods Reads

A single-page reading list (`index.html`). All entries live in the JSON block
`<script id="pulse-data">`; the field guide is in the comment just above it.

## Adding entries
- The user sends links grouped by month. Each entry goes into the edition for
  the month the user gives (e.g. "June 2026"), not necessarily its publication
  month. Create the edition if it doesn't exist, keep editions in date order,
  and set "latest" to the newest edition.
- The `source` line uses the actual publication date: "Organisation · Month Year".
- `genu` is shown as "Implications": write about what the piece means for
  youth livelihoods work in general, not specifically for GenU.
- Countries use the regions in REGIONS (e.g. India → "South Asia").
- Reuse existing theme tags where they fit.
- Leave `starred` false and omit `referenced` unless the user says otherwise.
- ScienceDirect and SSRN block automated access: ask the user to upload the PDF.
- Keep the JSON formatted as `json.dumps(indent=2, ensure_ascii=False)` output.
- Before pushing, open the page in a headless browser and check each changed
  edition renders with no errors.

## Publishing
Commit and push directly to `main` (the user asked for this; no pull request).
