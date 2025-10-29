# Webhook Inspector

A modern application to inspect, test and debug webhooks. This project is built using a monorepo structure with pnpm workspaces.

## Tech Stack

### Backend (API)
- [Fastify](https://fastify.io/) - Fast and low overhead web framework for Node.js
- [TypeScript](https://www.typescriptlang.org/) - JavaScript with syntax for types
- [PostgreSQL](https://www.postgresql.org/) - Open source relational database
- [Drizzle ORM](https://orm.drizzle.team/) - TypeScript ORM
- [Zod](https://zod.dev/) - TypeScript-first schema validation
- [Swagger/OpenAPI](https://swagger.io/) - API documentation

### Frontend (Web)
- [React](https://react.dev/) - JavaScript library for building user interfaces
- [TypeScript](https://www.typescriptlang.org/) - JavaScript with syntax for types
- [Vite](https://vitejs.dev/) - Next Generation Frontend Tooling

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v20 or higher recommended)
- pnpm (v10.20.0 or higher)
- PostgreSQL (v16 recommended)

## Getting Started

1. Clone the repository
```bash
git clone [repository-url]
cd webhook-inspector
```

2. Install dependencies
```bash
pnpm install
```

3. Configure environment variables
```bash
# Copy the example env file and update with your values
cp api/.env.example api/.env
```

4. Setup the database
```bash
cd api
pnpm db:generate
pnpm db:migrate
```

5. Start the development servers

In one terminal, start the API:
```bash
cd api
pnpm dev
```

In another terminal, start the web application:
```bash
cd web
pnpm dev
```

The API will be available at `http://localhost:3000` and the web application at `http://localhost:5173`.

## Available Scripts

### API
- `pnpm dev` - Start the development server with hot reload
- `pnpm start` - Start the production server
- `pnpm db:generate` - Generate database migrations
- `pnpm db:migrate` - Run database migrations
- `pnpm db:studio` - Open Drizzle Studio to manage the database

### Web
- `pnpm dev` - Start the development server
- `pnpm build` - Build the application for production
- `pnpm preview` - Preview the production build locally

## Documentation

The API documentation is available at `http://localhost:3000/docs` when running the development server.