# Issues to create

This file lists proposed issues to implement features inspired by the Activity-Dekho project. Each section has a title and a suggested body you can copy to GitHub Issues.

---

## 1. Auth: Add club authentication and session management

Add sign-in/sign-up flow for clubs, session persistence, and protected API endpoints. Include env config, session cookie or token handling, and basic tests.

Acceptance criteria:
- Club sign-in UI or API endpoint
- Session persistence across requests
- Protected routes for club admins

---

## 2. Persistence: Replace in-memory DB with Firestore (or other persistent store)

Replace the current in-memory `activities` dict with a persistent datastore. Provide Firestore integration (recommended) or an SQL alternative, with migrations and a README section for setup.

Acceptance criteria:
- Persistent storage for activities, participants, and events
- Configuration via `.env` and `.env.example`
- Basic integration tests

---

## 3. Events CRUD: Add UI and API to create/edit/delete events

Implement full CRUD for events: API endpoints and frontend forms/pages to create, edit, and delete events. Add validation and examples.

Acceptance criteria:
- Endpoints for create/edit/delete events
- Frontend forms or example pages to use them
- Input validation and error handling

---

## 4. Attendance: Advanced attendance management & reports

Add rich attendance features: add attendee records, attendance views, reporting, and CSV export. Include guest/family support and QR-based check-in as an extension.

Acceptance criteria:
- Add attendee API and UI
- View attendance per event with filters
- CSV export for reports

---

## 5. Filters & Reports: Implement DateFilters and reporting endpoints

Add `DateFilters` support (current/last semester, year, custom) and server-side reporting endpoints that return aggregated stats for date ranges.

Acceptance criteria:
- Server endpoints to query by DateFilters
- Client examples demonstrating the filters
- Unit tests for date calculations

---

## 6. State Management: Add client state orchestration (XState or similar)

Introduce XState or an equivalent for client-side orchestration for flows like club login, event editing and attendance workflows. Document the chosen pattern.

Acceptance criteria:
- At least one XState machine integrated (auth or events)
- Global state provider example

---

## 7. UI: Modernize frontend with Tailwind + modals + avatars + animations

Upgrade the static frontend to a modern component-based UI with TailwindCSS, animated modals, avatar generation and responsive layout. Provide a migration guide.

Acceptance criteria:
- Tailwind setup and example components
- Modal and avatar components
- Responsive styles for the activities list

---

## 8. DevOps: Add Dockerfile and GitHub Actions for deployment (Cloud Run)

Add a `Dockerfile` for the app and GitHub Actions workflows to build and deploy to Cloud Run (or another target). Include staging and production workflows.

Acceptance criteria:
- Working `Dockerfile` and `.dockerignore`
- GitHub Actions workflows for build and deploy
- README section with deploy steps
