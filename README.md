# Hostel Management

A local-first, role-aware foundation for a college hostel management platform. It uses React/Vite, Express, Prisma, and SQLite—no API keys or paid services.

## Start locally

```bash
npm install
cp server/.env.example server/.env
npm run db:generate
npm run db:migrate
npm run db:seed
npm run dev
```

The client runs at `http://localhost:5173`; the API runs at `http://localhost:4000`. The seed creates the single Super Admin from `server/.env` (`admin@hostel.local` / `ChangeMe123!` by default). Change those credentials before deployment.

## Current foundation

This initial implementation establishes the configurable hostel hierarchy, role-scoped authorization, account lifecycle, allocation history, issue workflow with duplicate prevention, immutable issue events, notifications, and audit logging. Schema changes should be applied with Prisma migrations; no physical rooms, floors, room types, equipment, or escalation settings are embedded in application code.
