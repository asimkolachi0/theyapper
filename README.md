# theYapper

A mobile-first social platform built with **Next.js**, **TypeScript**, and **Supabase**.

> A community-focused web app for sharing posts, discovering content, and connecting with other people.

## Overview

theYapper is a social networking project focused on a responsive experience across desktop, tablet, and mobile devices. The codebase uses Supabase for authentication and data persistence.

## Current features

- Responsive, mobile-first interface
- Social feed and post composer
- Search, likes, bookmarks, and follow toggles
- Email/password authentication with Supabase Auth
- Supabase-backed post reading and publishing
- Dark appearance toggle
- Database schema with Row Level Security for profiles, posts, follows, likes, comments, and bookmarks

## Tech stack

- **Framework:** Next.js
- **Language:** TypeScript
- **Backend and authentication:** Supabase
- **Deployment:** Vercel-compatible

## Run locally

### Requirements

- Node.js 18 or newer
- npm
- A Supabase project for persistent accounts and posts

### Setup

1. Clone this repository.
2. Install dependencies:

   ```bash
   npm install
   ```

3. Copy `.env.example` to `.env.local` and configure your Supabase project URL and publishable/anonymous key.
4. Run the SQL in `supabase/schema.sql` in your Supabase SQL Editor.
5. Start the development server:

   ```bash
   npm run dev
   ```

6. Open [http://localhost:3000](http://localhost:3000).

Without Supabase environment variables, the app can display sample content for preview. Authentication and persistent publishing require a configured Supabase project.

## Deploy

Import the repository into Vercel and configure these environment variables:

- `NEXT_PUBLIC_SUPABASE_URL`
- `NEXT_PUBLIC_SUPABASE_ANON_KEY`

Never expose a Supabase service-role key in a browser-accessible environment variable.

## Project status

This is an actively developing project. Some social features may still be placeholders or require further implementation before production use. Review and test authentication, database policies, and user interactions before launching publicly.

## Security notes

- Keep secrets and private credentials out of source control.
- Use environment variables for deployment configuration.
- Review Supabase Row Level Security policies before production deployment.

---

Built as an independent project by [@asimalikolachi123](https://github.com/asimalikolachi123).
