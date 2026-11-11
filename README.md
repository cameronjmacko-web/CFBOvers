# CFB Totals Lab — GitHub Pages package

## What this does

`index.html` loads shared, read-only CSVs from the `data/` folder. Visitors can use the lookup and predictor, but the page has no controls for changing the shared data. Predictions run in each visitor's browser.

Keep the GitHub repository public for GitHub Pages on GitHub Free. Leave repository write access with the owner only. Anyone can view the published site and download the public CSVs, but only repository collaborators with write permission can change the hosted data.

## Publish

1. Create a public GitHub repository.
2. Upload `index.html`, the whole `data/` folder, and this README to the repository root.
3. In **Settings → Pages**, select **Deploy from a branch**, choose `main` and `/(root)`, then save.
4. Open the Pages URL after deployment. Keep the `data/` folder next to `index.html`.

## Weekly owner update

- `data/team-form-history.csv`: append each new weekly snapshot. Keep earlier snapshot dates in the file so the predictor retains week-by-week form context.
- `data/game-results-history.csv`: append each week's completed games. Keep prior rows so Lookup history accumulates. The current file starts with Nov. 7, 2026 results; older lookup history is embedded in `index.html`.
- `data/current-slate.csv`: replace this with the upcoming slate each week.
- `data/team-form-2024-2025.csv`: static historical background; leave it unchanged unless you intentionally revise that context.

The CSV headers must stay compatible with the current files. A weekly refresh changes only the CSV files in `data/`; it does not require editing `index.html`.

## Access boundary

The webpage is public and read-only. GitHub repository permissions control who can update the shared CSVs. Do not add collaborators unless you want them to have write access. No GitHub token or password is included in the HTML.
