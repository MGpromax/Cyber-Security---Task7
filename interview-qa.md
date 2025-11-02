# Interview Q&A — Browser Extensions Security

## 1) How can browser extensions pose security risks?
- Data access: Many request permission to read and change data on visited sites, enabling content injection, data exfiltration, or credential capture.
- Tracking: Background scripts can monitor browsing behavior and phone home.
- Supply chain: Legitimate extensions can be sold and later updated with malicious code.
- Vulnerabilities: Poor coding practices can expose users to XSS or privilege abuse.

## 2) What permissions should raise suspicion?
- Read/change data on all websites (broad host permissions).
- webRequest / webRequestBlocking (traffic inspection/modification).
- Tabs, history, bookmarks (behavior tracking/manipulation).
- Clipboard, downloads, nativeMessaging, proxy, debugging.
- “Allow in Incognito” and “Access to file URLs” increase exposure.

## 3) How to safely install browser extensions?
- Use official stores (Chrome Web Store, AMO). Avoid sideloaded CRX/XPI.
- Verify publisher, install count, update history, and reviews.
- Prefer minimal permissions and transparent privacy policies.
- Review requested permissions at install; cancel if they’re excessive.

## 4) What is extension sandboxing?
- Browser isolates extensions from core processes and sites; content scripts run in isolated worlds with restricted APIs. MV3 uses service workers for background logic. Sandboxing reduces impact of bugs but does not prevent misuse of granted permissions.

## 5) Can extensions steal passwords?
- Yes, if granted permissions to read page content or intercept web requests on login pages. Good practice: keep password managers and critical sites whitelisted or minimize extension access on such pages.

## 6) How to update extensions securely?
- Keep auto‑updates on; update the browser itself.
- Periodically review change logs and permission changes after updates.
- Remove abandoned or suddenly permission‑escalating extensions.

## 7) Difference between extensions and plugins?
- Extensions: WebExtensions running inside the browser sandbox with declarative permissions.
- Plugins: Legacy NPAPI/PPAPI modules (e.g., Flash, Java) that ran outside the browser’s web sandbox; largely deprecated/removed in modern browsers.

## 8) How to report malicious extensions?
- Chrome: “Report abuse” on the Web Store listing or from `chrome://extensions` → Details → Report abuse.
- Firefox: “Report this add‑on” on the AMO listing or via the add‑on manager menu.
- Include evidence (version, publisher, suspicious behavior, screenshots/network traces).

Best Practices (quick list)
- Least privilege: install only what you need with minimal permissions.
- Verify publisher and reviews; avoid clones.
- Re‑audit regularly; remove unused extensions.
- Keep browser and extensions updated; enable safe browsing features.

