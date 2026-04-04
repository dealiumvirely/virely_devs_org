 # Virely Developer Portal — virely-devs.org

> **Enterprise Power. Small Business Heart.**  
> Official developer documentation portal for Virely LLC contractor engagements.

---

## Overview

This repository contains the source for **[virely-devs.org](https://virely-devs.org)** — the official Virely LLC developer portal. The portal serves as the single source of truth for all contractor developer policies, engagement standards, and project application procedures across the Virely platform family.

The portal is a single self-contained HTML file with no external dependencies beyond CDN-hosted fonts, making it simple to host, update, and version-control.

---

## Documents

The portal hosts two official policy documents:

### 1. Contractor Developer Engagement Policy
`SOP-DEV-001 · v1.1 · April 2026 · Confidential`

The binding standard operating procedure governing all Virely LLC software developer contractor engagements. Covers:

- Contract setup, onboarding, and eSign requirements
- Task creation, assignment, and the zero-scope-creep policy
- Milestone structure, submission, and CEO review/approval workflow
- Documentation standards (Jira, Otter AI, Slack, changelogs)
- Testing requirements — real device mandate, platform-specific checklists
- Time logging standards and the 5-business-day wage dispute window
- Standup call schedule (Tuesday & Thursday), async standup format
- Dispute policies and contractor rights
- Performance standards and industry benchmark timelines
- Security, access, and credential sharing prohibition
- Contractor vetting, NDA, and trial task policy
- Scope change management and change order process
- Version control and code delivery standards
- IP assignment, offboarding, and post-engagement obligations
- Professional conduct and developer interaction standards

### 2. Software Development Project Application Process
`Process Policy · v1.0 · April 2026`

The official process all developers — new and currently engaged — must follow to be considered for and awarded Virely development projects. Covers:

- Eligibility requirements (general and technical)
- Five-stage application process with timelines
- Interview format, evaluation criteria, and re-interview policy
- Selection criteria and weighting
- Project award, contract execution (48-hour window), and kickoff
- Policy for currently engaged developers applying to new projects
- Disqualification grounds and appeals process
- Confidentiality obligations

---

## Platforms Covered

Both documents apply to all work performed on Virely LLC technology properties:

| Platform | Domain | Type |
|---|---|---|
| Dealsby Reservations | [dealsbyreservations.com](https://dealsbyreservations.com) | SaaS — reservation management |
| Dealsby Appointments | [dealsbyappointments.com](https://dealsbyappointments.com) | SaaS — appointment scheduling |
| Dealsby Referrals | [dealsbyreferrals.com](https://dealsbyreferrals.com) | SaaS — referral marketing |
| Virely Books | As designated by CEO | Accounting & finance platform |
| Virely Nexus | As designated by CEO | Virely LLC platform |
| TheVirelyExperience.com | [thevirelyexperience.com](https://thevirelyexperience.com) | Experience & related landing pages |
| Virely Corporate | [virely.co](https://virely.co) | Corporate landing page & brand properties |
| Any future Virely platform | As designated by CEO | All new platforms added to the portfolio |

---

## Tech Stack

| Concern | Implementation |
|---|---|
| Format | Single-file HTML — no build step, no framework |
| Fonts | [Geist Sans & Geist Mono](https://vercel.com/font) via jsDelivr CDN |
| Styling | Vanilla CSS with custom properties |
| Interactivity | Vanilla JS — smooth scroll with sticky-header offset compensation |
| Hosting | Static file host (deploy `index.html` directly) |
| Dependencies | None beyond CDN fonts |

---

## Deployment

The portal is a single HTML file. Deploy by replacing the hosted `index.html` with the latest version of `virely-devs-updated.html`.

### Vercel (recommended)
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy from repo root
vercel --prod
```

### Manual / any static host
1. Rename `virely-devs-updated.html` → `index.html`
2. Upload to your static host (Vercel, Netlify, GitHub Pages, S3, etc.)
3. Point `virely-devs.org` DNS to the host

### Local preview
```bash
# Python
python3 -m http.server 8080

# Node
npx serve .
```
Then open `http://localhost:8080`.

---

## File Structure

```
virely-devs/
├── index.html                  # Production file — the full portal
├── README.md                   # This file
└── virely-devs-updated.html    # Working file (rename to index.html on deploy)
```

---

## Versioning

Document versions are tracked in the cover block of each policy document within the HTML. When updating policy content:

1. Increment the version number in the document cover metadata
2. Update the effective date
3. Commit with a message referencing the section changed — e.g., `docs: update Section 14 benchmark thresholds`

---

## Key Design Decisions

**Single-file architecture** — The entire portal (HTML, CSS, JS) lives in one file with no build tooling. This keeps deployment trivially simple and makes the document easy to share, archive, or print.

**Sticky header + offset scroll** — Anchor navigation compensates for the sticky header height so section titles are never obscured when jumping from the TOC.

**Geist font** — Matches the Virely platform family standard (not available on Google Fonts; loaded from jsDelivr CDN at `cdn.jsdelivr.net/npm/geist@1.3.1`).

**No localStorage / no client state** — The portal is a read-only policy document. No user data is collected or stored.

---

## Access & Confidentiality

This portal and its contents are **confidential**. Access is restricted to:

- Current and prospective Virely LLC contractor developers
- Virely LLC staff and leadership

Do not share the URL, repository link, or document contents with unauthorized parties. All content is subject to the confidentiality provisions of the Virely LLC Contractor Developer Engagement Policy (SOP-DEV-001).

---

## Contact

| | |
|---|---|
| **Organization** | Virely LLC (dba Dealsby) |
| **Department** | People & Talent Operations |
| **Website** | [virely.co](https://virely.co) |
| **Contractor Portal** | [virely.co/contractors](https://virely.co/contractors) |

---

<sub>© 2026 Virely LLC · Enterprise Power. Small Business Heart. · CONFIDENTIAL — INTERNAL USE ONLY</sub>
