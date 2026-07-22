# IT Support Prep — ElevenLabs TechSupport Engineer

Day-1 study app for the **ElevenLabs TechSupport Engineer (London)** role. Concepts pulled straight from the job description, with spaced repetition and auto-graded quizzes. Runs offline, saves per device.

## How to use

Open [index.html](index.html) in any browser — double-click it. No internet needed, progress saves automatically.

- **Two card types.** *Concept* cards (term ↔ definition) you flip and self-grade. *Quiz* cards (multiple choice) grade themselves — pick an answer, see if you're right plus a one-line why.
- **Spaced repetition.** Both card types feed one schedule. Mark/answer **got it** and the card returns on a widening ladder — **10 min → 1 day → 3 → 7 → 16 → 35 days**. Miss it and it resets to the start. The 10-minute first step means cards come back within your session.
- **⏰ Due** is the daily driver: every card that's come back due across all decks, drained as you clear it. Any other deck is free browsing.
- **★ Hard** collects the ones you keep missing — tap the star on any card.
- Keys: **Space** flip · **1** didn't know · **2** got it · **1–4** answer a quiz · **← →** move.
- **Term → Def** button flips concept cards to test recall (name the term from its definition) instead of recognition.

## The decks

| Deck | Covers |
|------|--------|
| 🧭 Framework | The troubleshooting loop (symptom → hypothesis → check → fix → verify) — the thing interviews actually test |
| 🎧 ElevenLabs | What the company does (Agents/Creative/API), culture, the role itself — interview prep |
| 🍎 macOS | System Settings vs Utilities, least privilege, Gatekeeper, FileVault, Keychain, Activity Monitor, Console, Terminal commands, Recovery/Safe Mode, APFS containers & volumes |
| 💿 Wipe & Rebuild | Clean install on a Lab volume, the secure-token gotcha, EACAS vs Recovery erase, Activation Lock |
| 💻 MDM & Devices | MDM, Apple Business Manager, zero-touch/ADE, supervised devices, remote wipe, lifecycle |
| 🌐 Networking | IP/DNS/DHCP, gateway, subnet, VPN, Wi-Fi bands, ports, TCP vs UDP, ping/traceroute |
| 🔑 SaaS & Identity | SSO, IdP, SAML/OIDC, MFA, SCIM, offboarding, least privilege |
| 📺 AV & Rooms | Zoom Rooms, HDMI vs USB-C, room audio/video troubleshooting order |
| ⌨️ Bash | Shebang, chmod, variables, loops, pipes, grep, posting to Slack (the bonus skill) |
| 🛠️ Support Skills | Troubleshooting method, escalation, SLAs, empathy, documentation |

## Live site

Published via GitHub Pages — every push to `main` redeploys automatically.

## Growing it

Content lives in the `DECKS` array at the top of the `<script>` in `index.html`.

- **Concept card:** `{t:"Term", d:"Definition/explanation."}`
- **Quiz card:** `{q:"Question?", opts:["A","B","C","D"], a:1, why:"Explanation."}` — `a` is the 0-based index of the correct option.

Add cards to any deck, or add a new deck `{id:"x", name:"🔧 Name", cards:[...]}`. That's it.
