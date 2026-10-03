# Flevaro — Web Application

Flevaro is a modern business management platform designed to help teams manage leads, sales activities, workflows, integrations, and daily operations from one workspace.

This repository contains the web application built with **Next.js** and **TypeScript**.

## Tech Stack

* **Framework:** Next.js
* **Language:** TypeScript
* **Frontend:** React
* **Styling:** Project-specific styling and UI components
* **API Communication:** Axios
* **Architecture:** Feature-based modules

## Getting Started

### Prerequisites

* [Node.js](https://nodejs.org/) — version compatible with the project
* npm, yarn, pnpm, or bun

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd flevaro-web
```

### 2. Install dependencies

Using npm:

```bash
npm install
```

Or use your preferred package manager:

```bash
yarn install
# or
pnpm install
# or
bun install
```

### 3. Configure environment variables

Create a `.env.local` file in the project root if the application requires environment variables.

```bash
touch .env.local
```

Add the required configuration, such as the backend API URL:

```env
NEXT_PUBLIC_API_URL=http://localhost:3000
```

Replace the URL with your deployed backend URL when configuring production.

> Only variables prefixed with `NEXT_PUBLIC_` are exposed to the browser. Never put private keys, passwords, or backend secrets in public environment variables.

### 4. Run the development server

```bash
npm run dev
```

Open http://localhost:3001 in your browser if the backend is already using port `3000`.

If port `3001` is unavailable, Next.js will report the port it uses.

## Available Scripts

Run the scripts defined in `package.json`:

```bash
npm run dev
npm run build
npm run start
npm run lint
```

* `dev` — starts the development server.
* `build` — creates a production build.
* `start` — runs the production server.
* `lint` — runs the project's lint checks, if configured.

## Project Structure

The application follows a feature-based structure to keep related pages, components, and logic organized.

```text
src/
├── app/          # Next.js routes and layouts
├── core/         # Shared API clients, components, hooks, and utilities
└── modules/      # Feature-specific application modules
```

### Main Application Areas

The frontend includes modules for:

* Authentication and user access
* Dashboard and overview
* Leads and lead assignment
* Ads and integrations
* Teams and staff management
* Follow-ups and activities
* Calls and call monitoring
* WhatsApp and inbox
* Broadcasts and automations
* Reports, exports, and notifications

The application structure may evolve as Flevaro is redesigned and developed.

## Backend Integration

Flevaro Web communicates with the Flevaro Node.js backend through API endpoints.

Make sure the backend is running and the frontend API URL is configured correctly before testing features that require server communication.

## Production Build

Create a production build:

```bash
npm run build
```

Start the production server:

```bash
npm run start
```

## Deployment

The application can be deployed on platforms that support Next.js, such as [Vercel](https://vercel.com/) or a suitable Node.js hosting environment.

For deployment instructions, refer to the [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying).

Configure the production environment variables in your hosting provider before deploying.

## Development Notes

* Keep frontend and backend environment variables separate.
* Do not commit `.env.local` or other files containing secrets.
* Keep reusable UI components in the shared core.
* Keep feature-specific logic within the relevant module.
* Validate API changes against the backend before releasing frontend updates.

## Project Status

Flevaro Web is the frontend application for the Flevaro platform. The existing CRM features will be reviewed, redesigned, and improved incrementally as the product evolves.
