# Next.js Dashboard App

Email: user@nextmail.com
Password: 123456

This project is a feature-rich dashboard application built with [Next.js](https://nextjs.org/) (App Router), [React](https://react.dev/), [Tailwind CSS](https://tailwindcss.com/), and [PostgreSQL](https://www.postgresql.org/). It is designed as a learning resource and starter template for building modern, full-stack web applications.

## Features

- **Authentication**: Simple login form (credentials-based, extendable with NextAuth.js)
- **Dashboard**: Overview cards, revenue chart, and latest invoices
- **Invoices**: List, search, create, edit, and delete invoices
- **Customers**: List and search customers, view invoice stats per customer
- **Responsive UI**: Mobile-friendly, accessible, and visually appealing
- **Skeleton Loaders**: Smooth loading states for dashboard and tables
- **Navigation**: Side navigation, breadcrumbs, and intuitive routing
- **Database Integration**: Uses PostgreSQL for data storage (with seed script)
- **Modern Stack**: Next.js App Router, React Server Components, Tailwind CSS, TypeScript

## Project Structure

```
app/
  layout.tsx           # Root layout
  page.tsx             # Landing page
  lib/                 # Data fetching, definitions, placeholder data, utils
  query/route.ts       # Example API route
  seed/route.ts        # Database seeding route
  ui/                  # UI components (dashboard, invoices, customers, etc.)
public/                # Static assets (images, favicon, etc.)
tailwind.config.ts      # Tailwind CSS configuration
postcss.config.js       # PostCSS configuration
next.config.ts          # Next.js configuration
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18+ recommended)
- [pnpm](https://pnpm.io/) (or use npm/yarn)
- [PostgreSQL](https://www.postgresql.org/) database

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repo-url>
   cd nextjs-dashboard
   ```
2. **Install dependencies:**
   ```bash
   pnpm install
   # or
   npm install
   # or
   yarn install
   ```
3. **Configure environment variables:**
   - Create a `.env.local` file in the root directory.
   - Add the following variable:
     ```env
     POSTGRES_URL=postgres://<user>:<password>@<host>:<port>/<database>
     ```

### Database Setup & Seeding

- To seed the database with sample data, start your database and run the seed route (see `app/seed/route.ts`). You can trigger this by visiting `/seed` in your browser or using an HTTP client.

### Running the App

- **Development:**
  ```bash
  pnpm dev
  # or
  npm run dev
  # or
  yarn dev
  ```
- **Production Build:**
  ```bash
  pnpm build && pnpm start
  # or
  npm run build && npm start
  # or
  yarn build && yarn start
  ```

## Scripts

- `dev` – Start the development server (with Turbopack)
- `build` – Build the app for production
- `start` – Start the production server

## Environment Variables

- `POSTGRES_URL` – Connection string for your PostgreSQL database

## Tech Stack

- **Framework:** Next.js (App Router), React
- **Styling:** Tailwind CSS, PostCSS, @heroicons/react
- **Database:** PostgreSQL (via `postgres` npm package)
- **Authentication:** Credentials (extendable with NextAuth.js)
- **TypeScript:** Full type safety

## Customization & Extending

- Add more pages, API routes, or UI components in the `app/` directory
- Extend authentication with [NextAuth.js](https://next-auth.js.org/)
- Replace placeholder data and logic with your own business logic

## License

This project is for educational purposes. See the [Next.js Learn Course](https://nextjs.org/learn) for more details.
