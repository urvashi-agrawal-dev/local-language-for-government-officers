# Seva — Income Certificate Review

**Seva** is a Hindi-language application review dashboard for government officers handling income certificate requests in West Bengal. It is an interactive prototype built for the Kenpath Full Stack AI Engineer assignment. All applicants, application IDs, and records are fictional.

## Demo access

Use these credentials on the Hindi sign-in screen:

- **Email:** `officer@seva.demo`
- **Password:** `Seva2026!`

This is a client-side demo gate for the assignment walkthrough, not real authentication. The credentials are visible in the frontend source and do not protect data or provide security.

## Problem and users

Income certificate applications can require officers to check several documents, resolve inconsistencies, and manage deadline pressure. This prototype helps an assistant district officer in the Ranaghat subdivision of Nadia district see which applications need attention and review each case in one place.

## What the application does

- Shows a dashboard of pending applications, overdue cases, and workload indicators.
- Lists applications by priority and deadline, with filtering and search by applicant, application ID, or locality.
- Opens an application detail view with a case summary, declared income, submitted documents, missing items, possible inconsistencies, and a suggested next step with reasons.
- Lets the officer approve, reject, or return an application for correction. A confirmation prompt appears before the decision is applied.
- Downloads the sample application list as a CSV file.
- Presents a Hindi sign-in screen with demo credentials.

## AI assistance and human decisions

The “AI assistance” in this prototype is made of predefined, explainable examples attached to fictional records. It does not call a live AI model, connect to a government database, or verify documents. Suggestions are advisory; the officer makes the final decision. A production version would need validated rules, traceable sources for each signal, audit logging, secure case storage, and human review.

## Technical decisions

- **HTML, CSS, and vanilla JavaScript:** keeps this small prototype easy to run without a build step, dependencies, or API keys.
- **Hindi-first interface:** the dashboard, sample case details, actions, and status labels are in Hindi. It uses Noto Sans Devanagari from Google Fonts with system-font fallbacks.
- **Local fictional data:** eight sample applications are defined in `app.js`. Decisions update the queue in the current browser session; refreshing restores the demo data.
- **Prototype scope:** no backend, persistent case storage, live AI, PDF reporting, or government-system integration.

## Run locally

No dependencies are required. Open `index.html` in a browser, or start a static server from the project directory:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`. Sign in with the demo access credentials above.

## Demo context

- Service: income certificate applications
- District: Nadia, West Bengal
- Subdivision: Ranaghat
- Sample records: eight fictional applications
- Demo officer: Urvashi Sen, Assistant District Officer

## Potential next steps

Before real-world use, validate the service rules and required documents with the relevant department. Replace the demo gate with server-side authentication and add role-based access, audit trails, privacy safeguards, persistent case storage, and source-backed AI suggestions with officer review.

