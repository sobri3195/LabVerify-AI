# LabVerify-AI

**Every completed result has a next owner.**

LabVerify-AI is a polished research and showcase prototype for automated operational assignment, acknowledgement monitoring, and escalation of completed emergency-department laboratory results. It coordinates responsibility; it does **not** diagnose, interpret laboratory values, verify results, prescribe treatment, determine discharge, or represent a certified medical device.

All people, patient aliases, records, events, metrics, and outcomes are synthetic. No paid services, database, backend, API key, or real patient data are required.

## Quick start

```bash
npm install
npm run dev
```

Open `http://localhost:5173`. Use **Fast Login as Demo Admin** or preview the ED Physician, Laboratory Supervisor, and Operations Manager roles. The visible form is prefilled for demonstration with `admin@labverify.ai` / `LabVerify2026!`; authentication is entirely local and stores only a non-sensitive role session.

## What is included

- Public landing, about, interactive case study, methodology, privacy, and login routes.
- Protected command centre with result queue/detail, alerts, physicians, cases, analytics, audit, reports, and settings.
- 120 generated laboratory workflow records, 18 fictional physicians, 35 alerts, 150 audit events, 12 alias-only ED cases, eight test groups, three shifts, four roles, and 30 analytics days.
- Deterministic eligibility and weighted assignment (availability 35%, workload 30%, acknowledgement history 20%, recency 15%; authorisation is a mandatory gate).
- A clearly labelled synthetic, non-clinical delay-risk demonstration.
- Local acknowledgement, defer, reassign, escalate, close, CSV export, notification preview, scenario playback, theme, reduced-motion, policy, surge, reset, and demo controls.

## Quality commands

```bash
npm run lint
npm run typecheck
npm run build
```

## Architecture

The React + strict TypeScript app is built with Vite, React Router, Tailwind CSS, Motion, Recharts, Lucide, TanStack Table and Query, React Hook Form, Zod, date-fns, and Sonner. `src/data/fixtures.ts` deterministically generates the synthetic fixture volume. `AppState.tsx` supplies a browser-only mock service/state layer and persists safe demo actions and preferences to LocalStorage.

## Deployment

The repository is ready for Vercel:

- Install: `npm install`
- Build: `npm run build`
- Output: `dist`

`vercel.json` rewrites nested routes to `index.html`, supporting direct refreshes across React Router routes.

## Privacy and limitations

This is a workflow simulation, not a medical device or clinical AI system. It provides no decision support or care recommendation. Synthetic performance figures are illustrative and must not be read as evidence of clinical, operational, or financial effectiveness. Browser notification and SMS/WhatsApp controls are previews; no external message is sent. Clear browser storage from Settings using **Restore defaults** or the browser's storage controls.
