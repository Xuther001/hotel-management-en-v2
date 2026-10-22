# Haven Group — Mobile Hotel Management

A responsive hotel management application for managing hotel operations across multiple properties.

## Requirements

- Node.js 20.19+ or 22.12+
- npm

## Run locally

Install dependencies:

    npm ci

Start the frontend and API:

    npm run dev

Open the frontend at http://localhost:5173.
The local API defaults to port 4000, and Vite proxies `/api` requests to it during development.

## Configuration

The frontend supports `VITE_API_URL` for connecting to a separately hosted API. When unset, API requests use the same origin; the Vite proxy is used during local development.

The API supports these environment variables:

- `PORT` — API listening port (default: `4000`)
- `DATA_FILE` — path to the persistent JSON data file
- `PUSH_SUBSCRIPTIONS_FILE` — path to push notification subscriptions

Do not commit `.env` files, credentials, push subscriptions, or real hotel data. Never put server secrets in `VITE_*` variables.

## Build

    npm run build

The production frontend is generated in `dist/`.

## Important security note

Before exposing the API publicly or using real guest information, ensure authentication, authorization, input validation, secure data storage, and appropriate backups are in place. A successful frontend build does not prove that the backend is production-secure.
