# Clarity from Confusion — Scrollytelling Site

An interactive, scroll-driven retelling of the survey paper *"Clarity from Confusion: A Survey of Design Choices for Machine Learning Performance Visualization"* (Spivak, Creamer, Tory & Borkin, IEEE TVCG 2024).

It's a **single static `index.html`** — no build step, no dependencies except Google Fonts. That makes it ideal for GitHub Pages.

## What's inside
- Animated hero with the confusion-matrix motif (TP / FP / FN / TN)
- An interactive confusion matrix (click a cell)
- Metric "anatomy" cards (Accuracy, Precision, Recall, Specificity, F1, ROC/AUC)
- A sticky scrollytelling module for the encoding-frequency findings (n = 490)
- Animated donut (accuracy 35.3% + confusion metrics 19.5%)
- Animated line chart of visualizations per year (2019–2023)
- Count-up stat band + the axis-inconsistency finding (26 / 3 / 13)
- Visual-channel bars and a closing call-to-action

---

## Deploy on GitHub Pages

### Option A — through the GitHub website (no command line)
1. Create a new repository on GitHub (e.g. `clarity-from-confusion`). Make it **public**.
2. Click **Add file → Upload files**, drag in `index.html` (and this `README.md`), and commit.
3. Go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Pick branch **`main`** and folder **`/ (root)`**, then **Save**.
6. Wait ~1 minute. Your site goes live at:
   `https://<your-username>.github.io/<repository-name>/`

### Option B — with Git on the command line
```bash
# from the folder containing index.html
git init
git add index.html README.md
git commit -m "Add scrollytelling site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repository-name>.git
git push -u origin main
```
Then do steps 3–6 from Option A to turn Pages on.

### Custom domain (optional)
In **Settings → Pages → Custom domain**, enter your domain and add the matching DNS records your registrar requires. GitHub will provision HTTPS automatically.

---

## Editing
- All content, styling, and logic live in `index.html`.
- Colors are CSS variables at the top (`:root`) — `--tp`, `--fp`, `--fn`, `--tn` drive the whole palette.
- Chart numbers are in the markup (`data-w`, `data-count`) and in the `<script>` data arrays (line chart, donut percentages).

## Attribution
This page is an independent educational visualization of the paper's findings. All statistics are drawn from:

> S. Spivak, M. Creamer, M. Tory, and M. A. Borkin. "Clarity from Confusion: A Survey of Design Choices for Machine Learning Performance Visualization." *IEEE Transactions on Visualization and Computer Graphics*, 2024.
