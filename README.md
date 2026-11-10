# Melhem Salloum website update

## Files
- `index.html` — responsive professional homepage and searchable publication library.
- `updates.json` — publication/update records shown on the homepage.
- `card.html` — supplied interactive business card, retained as a separate page.
- `profile.jpg` — copy your existing professional portrait into this folder before publishing. The homepage and card page expect this exact filename.

## Publish on GitHub Pages
1. Open the repository `1973M73/melhemwebsite` on GitHub.
2. Back up or download the current repository before replacing files.
3. Upload/replace `index.html`, `card.html`, `updates.json`, and `README.md` in the repository root. Keep existing assets and other pages unless you intentionally want to replace them.
4. Upload your portrait as `profile.jpg` in the repository root (the existing card expects that path).
5. Commit the changes to the branch configured for GitHub Pages (usually `main`).
6. Wait for GitHub Pages to finish deploying, then test the homepage and `/card.html` on both desktop and mobile.

## Add a new publication or update
Open `updates.json` and add another object inside the outer array. Example:

```json
{
  "title": "Exact publication title",
  "category": "AI Governance",
  "date": "2026-11-05",
  "summary": "A short factual description of the work.",
  "url": "https://doi.org/your-doi",
  "linkLabel": "Open publication ↗",
  "tags": ["AI", "governance", "research"]
}
```

Use one of these categories for the built-in filter: `Governance Psychology™`, `GRC & Risk`, `AI Governance`, `EGIA™`, `MENTALITY`. Dates must use `YYYY-MM-DD`. If no confirmed publication date is available, omit `date`. Keep JSON syntax valid (commas between objects; no trailing comma after the last object). Save and commit the file; the page updates automatically after deployment.

## Important
This is a static GitHub Pages implementation. It does not contain an online admin login or write access to GitHub, because embedding a GitHub access token in public browser code would expose repository credentials. Updates are managed safely by editing `updates.json` in the authenticated GitHub repository. An authenticated CMS/admin panel can be added later using a secure OAuth-backed service.
