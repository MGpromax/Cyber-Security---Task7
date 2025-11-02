# Cyber Security Internship — Task 7: Identify and Remove Suspicious Browser Extensions

Objective
- Learn to identify risky/unused browser extensions and remove them safely. Document what was found, actions taken, and improvements observed.

Scope & Tools
- Browsers: Google Chrome (Chromium‑based) and Mozilla Firefox
- Pages: `chrome://extensions` (Chrome) and `about:addons` (Firefox)
- Evidence: screenshots (before/after), list of extensions audited, notes on permissions, actions taken

What this repo contains
- `task7/procedure.md` — detailed, step‑by‑step auditing and removal process
- `task7/findings.md` — template to record suspicious/unused extensions and actions
- `task7/interview-qa.md` — concise answers to likely interview questions

Executive Summary (fill after your audit)
- Environment: [Chrome/Firefox versions]
- Audited extensions: [count]
- Removed/disabled: [count]
- Key reasons: [e.g., excessive permissions, poor reviews, unused, sideloaded]
- Observed improvements: [e.g., faster start, reduced CPU/memory/network]

Method Summary
1) Inventory installed extensions via the browser’s extensions manager.
2) Evaluate each extension’s permissions, legitimacy, usage, reviews, update history.
3) Disable or remove anything unused or suspicious. Prefer remove over disable when in doubt.
4) Restart the browser and check performance via built‑in task manager and subjective responsiveness.
5) Document findings, rationale, and outcomes in `task7/findings.md` and add screenshots.

Safety and Privacy
- Do not share personal data in screenshots. Redact emails, profile names, and private URLs.
- Only install from official stores. Avoid sideloading CRX/XPI from unknown sites.

How to reproduce
- Follow `task7/procedure.md` on your system. Capture before/after screenshots of extension lists and task manager metrics.

Submission
- Add your screenshots to a `screenshots/` folder.
- Update `task7/findings.md` with your actual results.
- Commit and push to a new GitHub repo, then submit the repo link in your portal.

