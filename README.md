# Smart Task Manager (Next.js + Prisma + NextAuth)

Faculty can create/assign tasks to students; students can update progress. Includes deadlines, statuses, notifications, and secure login.

## Quick Start

1. **Install deps**
   ```bash
   npm install
   ```
2. **Configure env**
   ```bash
   cp .env.example .env
   # Generate a secret
   # mac/linux
   openssl rand -base64 32
   # paste into NEXTAUTH_SECRET in .env
   ```
3. **Init Prisma**
   ```bash
   npx prisma migrate dev --name init
   ```
4. **Seed demo users**
   Start dev server, then in another terminal:
   ```bash
   npm run dev
   # In a new terminal:
   curl -X POST http://localhost:3000/api/users
   ```
5. **Sign in**
   - Faculty: `ada@uni.edu` / `password`
   - Student: `grace@uni.edu` / `password`

## Scripts
- `npm run dev` – start Next.js dev server
- `npm run build` – production build
- `npm run start` – start production server

## Tech
- Next.js App Router, React, TypeScript, Tailwind
- Prisma ORM (SQLite by default; switch DATABASE_URL for Postgres/MySQL)
- NextAuth Credentials Provider
- Zod validation
