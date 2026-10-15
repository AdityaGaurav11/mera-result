# MyJob redesign package

## Included files
- `index.html` — responsive MyJob homepage; reads listing data from `data.json`.
- `data.json` — syntactically valid starting dataset with official portal links and empty job/result/admit/exam categories.
- `admin.html` — local listing editor. Add/delete items and export an updated `data.json`.
- `backup/index.html` and `backup/data.json` — exact copies of the original files fetched from `AdityaGaurav11/mera-result` before redesign. The original `data.json` is malformed; it is intentionally preserved as a backup, not used by the new homepage.

## Publish to GitHub
1. Open `https://github.com/AdityaGaurav11/mera-result`.
2. Upload/replace `index.html` and `data.json` from this package.
3. Add `admin.html` and the `backup/` files too, or upload the entire package contents while preserving the directory structure.
4. Commit the changes.
5. In repository Settings → Pages, confirm the intended branch and folder are configured as the publishing source.
6. Open the published website and test the search and official links.

## Updating listings
1. Open the published `admin.html` page or run the package through a local web server.
2. Upload the current `data.json` with the file picker.
3. Add/delete listings, then click **Export data.json**.
4. Commit the exported file to the repository to publish changes.

## Important limitations
- This version is a static website. The data manager edits a local draft and exports JSON; it does not write to GitHub automatically.
- There is no secure admin login, shared database, or shared candidate-query inbox yet. Candidate queries/replies require a backend (for example, a database with row-level security and authenticated admin access) and configuration.
- Only generic official portal links are seeded. They are not claims that a specific vacancy, result or admit card is currently available. Add verified notices and dates before promoting them.
- Never store service-role keys, passwords, or other secrets in client-side HTML/JavaScript.
