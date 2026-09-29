# FraudLens Prototype

Explainable AI fraud detection dashboard (HackMatrix 5.0 prototype).
Plain HTML, CSS and JavaScript. No install or build step needed. All data is synthetic.

## Run in VS Code
1. Unzip the folder and open it in VS Code (File > Open Folder).
2. Install the **Live Server** extension (Ritwick Dey).
3. Right-click `index.html` and choose **Open with Live Server**.

Alternative: double-click `index.html`, or run `npm start` if Node.js is installed.

## Demo flow
1. Click **Sign In** (demo login, no real check).
2. Dashboard: stats, trend chart, alert distribution, recent alerts.
3. Alerts: filter by High, Medium or Low, then click alert **#1042**.
4. Alert detail: Overview (why it was flagged), Graph View, Timeline, Evidence, Comments.
5. Graph View: click nodes in the entity graph.
6. Reports (Investigation): download evidence, save notes, **Mark as Investigating**.
7. Settings: toggles and Logout.

## Project structure
- `index.html` - page shell
- `css/style.css` - blue and white theme (colours are CSS variables at the top)
- `js/app.js` - screens, sample data and navigation

## Customising
- Sample alerts, transactions: `AL` and `TX` arrays at the top of `js/app.js`.
- Sidebar menu: `NAV` array.
- Team name / branding: search for "FraudLens" in `js/app.js`.

## Note for judges
Scores, graph and timeline are hard-coded for the demo. The full system would compute them
with Python, a graph database, Isolation Forest and SHAP explanations.
