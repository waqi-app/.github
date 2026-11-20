# WAQI — Unified Scam Prevention for Egypt

One app, one verdict, explained in plain language. Graduation project, FCIS Ain Shams 2026–2027.

**The problem:** scams in Egypt are met with awareness campaigns. They inform, but they don't protect at the moment a scam arrives. WAQI acts at that moment: it checks the message, link, QR code, or receipt for you.

## Repos

| Repo | What it is |
|---|---|
| [waqi-app](https://github.com/waqi-app/waqi-app) | React Native app + native Android modules, Supabase backend, Dockerized link/QR sandbox |
| [waqi-ml](https://github.com/waqi-app/waqi-ml) | Egyptian-Arabic message NLP, receipt forensics, XGBoost + SHAP orchestrator |
| [waqi-website](https://github.com/waqi-app/waqi-website) | Public landing page (this org profile links to it) |
| [WAQI-QR](https://github.com/waqi-app/WAQI-QR) | QR awareness campaign: tracking, scam simulation, admin dashboard |

Team workflow lives in each repo's `WORKFLOW.md`: `dev` is default, feature branches + PR review, no direct pushes to `main`/`dev`.

## Live

- Website: https://waqi-app.github.io/waqi-website/
