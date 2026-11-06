# Security Maturity Assessment Tool

A lightweight, browser-based tool that scores an organisation's security posture and produces a prioritised one-year improvement roadmap. It is a single HTML file with no backend, no build step and no external dependencies.

## What it does

- Asks 24 questions across the six NIST CSF 2.0 functions: Govern, Identify, Protect, Detect, Respond and Recover.
- Scores each answer from 0 (not in place) to 4 (optimised), weighted by impact.
- Assigns an overall maturity level from Level 1 (Initial) to Level 5 (Optimised).
- Applies critical-control caps: if a critical control such as MFA, backups or an incident response plan is below Managed, the overall level is capped.
- Generates a four-quarter roadmap ordered by impact against effort, with dependencies respected (for example, asset inventory before vulnerability management).
- Shows a radar chart of domain scores, a suggested owner and cost band per action, and a sector option that boosts the most relevant domains.
- Saves your last result in the browser and compares it with the next assessment.
- Prints or saves the results as a PDF from the browser.

## Usage

Open `index.html` in any modern browser, or host it on any static host such as GitHub Pages, Netlify or Cloudflare Pages. Answer all questions, then select **Calculate maturity**.

## Customising

All questions, weights, effort ratings, control IDs, dependencies and sector boosts live in the arrays at the top of the script (`Q`, `OWN`, `COST`, `BOOST`). Edit them to fit your own framework or audience.

## Data and privacy

Everything runs locally in the browser. No answers are sent anywhere. Saved results are stored in the browser's local storage on the device you use.

## Limitations

- Self-assessments tend to be optimistic, so the result is only as accurate as the answers given.
- Control IDs are indicative NIST CSF 2.0 mappings and should be verified before formal use.
- Sector boosts are a general judgement, not a regulatory
