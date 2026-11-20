# WAQI: A Unified Scam Prevention Application

**One app that checks every channel scammers use in Egypt, and gives you one clear answer.**

WAQI is a graduation project by a team of 6. It's built to catch scams that span several channels at once: a fake InstaPay screenshot on WhatsApp, a cloned website behind a QR code, a scam call followed by a text from the same number.

## Who it's for

People in Egypt who get paid informally through **InstaPay, Vodafone Cash, or Orange Cash**: small sellers, delivery workers, freelancers, and online sellers on Instagram and Facebook Marketplace. They need to know a payment is real before releasing goods or services. The call, message, and link protection features keep the same users safe from the scams around that moment.

## How it works

WAQI isn't five separate tools bolted together. Each engine extracts raw signals, not verdicts. A central orchestrator combines all of them into a single **risk score, scam type, and confidence**, and explains the result in plain language.

| Engine | What it does |
|---|---|
| **Call Protection** | Checks incoming numbers against a crowd-sourced scam number database |
| **Message Protection** | Detects scam intent in SMS and WhatsApp messages, including Egyptian Arabic and Arabizi |
| **Link & QR Sandbox** | Opens links and QR destinations in an isolated container, follows the redirect chain, and reports what the page really is |
| **Receipt Forensics** | Detects fake or manipulated payment screenshots in Egyptian payment formats |
| **Orchestrator** | Fuses all signals with XGBoost, explains the decision with SHAP, and uses an LLM only to narrate it |

All engines also write to a shared correlation store, so a number reported on a scam call is flagged instantly if it later shows up in a WhatsApp message.

## Privacy

- The link sandbox never stores screenshots. Only the plain-language explanation of the site is kept.
- Receipt analysis stores extracted text only, never the images.

## Repositories

| Repo | What's in it |
|---|---|
| [`waqi-app`](../../waqi-app) | React Native app, Android native modules, Supabase migrations and functions, the Docker link/QR sandbox, docs and the project website |
| [`waqi-ml`](../../waqi-ml) | Training and evaluation code for the message model, receipt forensics, and the orchestrator |

Datasets and trained models live in our private Hugging Face organization, not in git.

## Contributing

`dev` is the default branch and `main` is production. Work on a feature branch, open a PR into `dev`, and get a review. Each repo's `WORKFLOW.md` has the full team rules.

## Project site

Documentation and an overview of the project: *(link to the GitHub Pages site once it's live)*
