# Lead Management & Email Tracking System

Lead Management & Email Tracking System is a Next.js app for capturing leads, emailing them automatically, and tracking engagement with open and click events.

## What it does

- Collects lead submissions through a responsive form
- Stores lead data in MongoDB via Mongoose
- Sends follow-up emails with Resend
- Tracks email opens with a tracking pixel
- Tracks link clicks through redirect URLs
- Surfaces lead and email metrics in a dashboard
- Classifies leads with a simple AI-ready categorization layer

## Tech Stack

- Next.js 15 App Router
- React 19
- TypeScript
- Tailwind CSS
- MongoDB and Mongoose
- Resend
- React Hook Form and Zod
- Recharts

## Project Structure

```text
src/
├── app/
│   ├── api/
│   │   ├── dashboard/
│   │   ├── leads/
│   │   └── track/
│   ├── dashboard/
│   ├── layout.tsx
│   ├── page.tsx
│   └── globals.css
├── components/
├── lib/
├── models/
├── services/
└── types/
```

## Environment Variables

Create a local environment file with the following values:

```env
MONGODB_URI=
RESEND_API_KEY=
NEXT_PUBLIC_APP_URL=
REDIRECT_URL=
DB_NAME=
EMAIL_FROM=
EMAIL_SUPPORT=
TRACKING_BASE_URL=
```

## Deployment

The project is configured for Vercel deployment. After connecting the GitHub repo, pushes to `main` should create production deployments automatically.

## Notes

- API routes live under `src/app/api`
- Shared business logic lives in `src/services`
- Database models are in `src/models`
- Shared types and schemas are in `src/types`
