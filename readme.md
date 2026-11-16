# 📈 EdgeJournal — Institutional Trading Journal & Risk Analytics

**EdgeJournal** is a fast, zero-backend, dark-mode trading journal and risk management web application inspired by TradeZella. Built as a single self-contained HTML file, it provides institutional-grade trade analytics, position sizing, drawdown circuit breakers, and psychological journaling—with 100% private, local browser storage.

---

## ✨ Key Features

### 1. 📊 Executive Dashboard & Performance KPIs
* **Core Telemetry Cards:** Tracks **Net P&L** (with equity sparkline), **Trade Win %**, **Profit Factor**, **Avg Win / Avg Loss Ratio**, and a composite **Edge Score (0–100)** radial gauge.
* **Interactive Visualizations:**
  * **Cumulative Net P&L & Drawdown Curve:** Dual-series equity curve built with Chart.js.
  * **Daily Net P&L Bar Chart:** Session-by-session profit and loss distribution.
  * **Monthly P&L Heatmap:** Interactive calendar overview of green and red trading days.

### 2. 🛡️ Risk Management & Position Sizing Suite
* **Pre-Trade Position Size & Lot Calculator:**
  * Tailored pip/point calculations for **XAUUSD (Gold)**, **EURUSD/GBPUSD**, **NQ/US100 Futures**, **ES/SPX500 Futures**, and **BTCUSD**.
  * One-click **Sync Live Equity**, quick risk presets (`0.25%`, `0.5%`, `1%`, `2%`), bidirectional price-to-pip conversion, Planned R:R calculation, and 1-click copy.
* **Live Circuit Breakers & Guardrails:**
  * Configurable thresholds for **Max Risk Per Trade (%)**, **Daily Max Loss ($)**, **Rolling 5-Day Weekly Drawdown ($)**, **Consecutive Loss Lockout**, and **Max Trades Per Day**.
  * Real-time status indicators (`SAFE` / `WARNING` / `BREACHED`) synced across the top header and navigation bar.
* **R-Multiple & Expectancy Analytics:**
  * Tracks System Expectancy (`$` and `R`), Max Peak-to-Valley Drawdown, Consecutive Streak counters, a **Planned vs. Realized R-Multiple Histogram**, and a **Historical Risk Compliance Audit** table.

### 3. 📝 Master Trade Log & Execution Replay
* **Multi-Faceted Filtering:** Filter executions by account, date range, symbol, direction (`LONG`/`SHORT`), playbook setup, mistake tag, or outcome.
* **Interactive Trade Detail Modal:**
  * Synthetic candlestick price-action replay showing **Entry**, **Exit**, **Stop Loss**, and **Take Profit** levels.
  * Interactive **Playbook Rule Checklists**, **Mistake & Psychology Tags** (*FOMO*, *Moved Stop*, *Early Exit*, *Overleveraged*, *Chased Entry*), 5-star execution ratings, and auto-saving review notes.
* **Bulk CSV Import:** Paste and import broker executions directly into your log.

### 4. 📅 Full Calendar & Daily Session Journal
* 8-column monthly calendar featuring daily P&L, trade count, win rate, and an automated **Weekly Summary** column.
* Click any calendar date to log your **Pre-Market Gameplan**, **Post-Session Reflection**, and **Daily Process Checklist**.

### 5. 🎯 Strategy Playbooks & Deep Reports
* **Playbook Edge Verification:** Automatically computes Win Rate, Profit Factor, Expectancy, and Net P&L per strategy.
* **Analytics Reports:** Visualizes Net P&L by Setup, Cost of Behavioral Mistakes (`$`), Performance by Day of Week, and Long vs. Short directional edge.

---

## 🔒 Privacy & Data Storage

* **100% Local & Private:** EdgeJournal has no backend server or external database. All trades, risk rules, playbooks, and daily notes are stored locally in your browser via `localStorage`.
* **Multi-User Safe:** When hosted publicly (e.g., via GitHub Pages), every visitor gets their own private instance stored exclusively on their own device.
* **Resetting Demo Data:** The app ships with pre-populated sample trades across Gold (`XAUUSD`), Indices (`NQ`, `ES`), Forex (`EURUSD`), and Crypto (`BTCUSD`). Click **Reset Demo Data** in the bottom-left sidebar at any time to restore the default dataset.

---

## 🚀 Hosting for Free on GitHub Pages

1. Create a new **Public** repository on GitHub (e.g., `edgejournal`).
2. Upload `index.html` and `README.md` to the root of the repository.
3. Go to **Settings** → **Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
5. Select the `main` branch and `/ (root)` folder, then click **Save**.
6. Within 1–2 minutes, your live app will be accessible at:
   ```text
   https://<your-username>.github.io/edgejournal/
   ```

---

## 🛠️ Tech Stack

* **HTML5 & Vanilla JavaScript (ES6+)** — Zero build steps, zero dependencies to install.
* **Tailwind CSS (CDN)** — Responsive obsidian dark-mode UI with `tabular-nums` financial alignment.
* **Chart.js** — Equity curves, daily P&L histograms, R-multiple distributions, and setup breakdowns.
* **Lucide Icons** — Crisp vector iconography.
