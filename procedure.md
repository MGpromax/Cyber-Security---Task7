# Task 7 — Procedure: Identify and Remove Suspicious Browser Extensions

Important: Act cautiously. If an extension is required for work, verify with your admin before removal.

Prerequisites
- Update your browser to the latest version.
- Close unrelated tabs. Consider taking a backup or note of extension names in case you want to reinstall later.

What to collect (for documentation)
- Before: full list of extensions with name, ID, version, permissions.
- After: list of disabled/removed extensions and why, plus any performance changes.
- Screenshots: before/after lists and task manager metrics.

Chrome (Chromium‑based)
1) Open manager: type `chrome://extensions` in the address bar.
2) Enable Developer mode (top‑right) to reveal extension IDs and background info.
3) For each extension, click “Details” and review:
   - Permissions: Look for high‑risk ones like “Read and change all your data on the websites you visit”, clipboard, downloads, history, tabs, webRequest, proxy, nativeMessaging.
   - Site access: “On all sites” is higher risk than “On click” or specific sites.
   - Source: Confirm “View in Chrome Web Store” link; avoid sideloaded/unverified sources.
   - Publisher and last updated date: long‑abandoned or brand‑new clones can be risky.
   - Reviews: check for recent negative reports, suspicious spikes, or copycat listings.
4) Decision tree:
   - Unused → Remove.
   - Excessive permissions without clear need → Remove or replace with a safer alternative.
   - Unknown developer, poor reviews, sideloaded → Remove immediately.
5) Remove or disable:
   - Prefer “Remove” for anything suspicious. Use “Toggle off” only if you must keep it temporarily.
6) Restart Chrome.
7) Measure improvements:
   - Open Chrome Task Manager (Shift + Esc) to compare CPU/memory footprint before vs after.

Firefox
1) Open manager: type `about:addons` → “Extensions”.
2) For each extension, click the three‑dot menu → “Manage” and review:
   - Permissions requested.
   - Author, homepage, last updated date.
   - “Permissions” and “More information” links to AMO (addons.mozilla.org) listing.
3) Decision tree mirrors Chrome (unused, excessive permissions, unknown publisher → remove).
4) Remove or disable via the extension menu.
5) Restart Firefox.
6) Measure improvements via `about:performance` or the OS task monitor.

How to evaluate risk (quick rubric)
- Necessity: Is it actively used and critical?
- Legitimacy: Official store listing, verified publisher, clear privacy policy.
- Permissions: Minimal required vs broad access to all sites/data.
- Popularity & reviews: Organic history vs sudden clones/spam.
- Behavior: Unexpected pop‑ups, redirects, injected ads, high resource use.

Advanced checks (optional)
- Chrome: On `chrome://extensions`, click “Service worker” (if present) then open DevTools to inspect network activity the extension initiates.
- Review the Web Store/AMO change log for recent permission escalations.
- If enterprise‑managed, review admin policies and logs before removal.

Documentation & Evidence
- Record each extension’s Name, ID, Version, Permissions, Action (Kept/Removed), and Rationale in `task7/findings.md`.
- Add screenshots to a `screenshots/` folder (redact sensitive info).

Post‑removal checklist
- Browser starts faster and fewer CPU spikes.
- No unexpected ads, redirects, or search hijacks.
- Extensions left have clear purpose and minimal permissions.

