# Omini — Frontend

This is the Next.js dashboard for Omini, a unified inbox that lets an online shop manage its Telegram, WhatsApp, and Instagram customer messages from one place, with AI-assisted classification and auto-replies.

The full project description, architecture explanation, and AI-usage disclosure required for CS50 live in the backend repository's README, since that's where the core logic (webhook handling, the AI agent, authentication, and the payment flow) actually runs: https://github.com/AMINB123/omini_backend

## What's in here

- `app/(site)/` — the public marketing pages: landing page, login, registration, and password reset, sharing one header/footer layout.
- `app/dashboard/` — everything behind login: the conversation inbox (grouped by customer, with manual reply support), the analytics page (charts built with Recharts), the subscription/payment page (with a live countdown to expiry), and store settings (business info and Telegram bot connection).
- `app/components/` — shared UI pieces: the logo (an SVG built from three platform-colored arcs), the header, footer, and sidebar.
- `app/lib/api.ts` — a small wrapper around `fetch` that attaches the access token to every request and silently refreshes it using the refresh token if the backend returns a 401, instead of forcing the user to log in again every 30 minutes.

Built with Next.js (App Router), TypeScript, Tailwind CSS, and Recharts.
