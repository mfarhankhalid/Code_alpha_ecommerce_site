# Code_alpha_ecommerce_site
# Aurelia Store

A full-stack e-commerce web app built with Next.js, TypeScript, and PostgreSQL. Includes product browsing, cart, checkout, user authentication, and order history.

> 🎓 **Internship Project — CodeAlpha**
> This project was developed as part of my Web Development internship at [CodeAlpha](https://www.codealpha.tech/).

## Features

- 🛍️ Product catalog with categories, ratings, and stock tracking
- 🛒 Cart and checkout flow (cash on delivery)
- 🔐 Email/password authentication with secure session cookies
- 📦 Order history and confirmation pages
- 🗄️ PostgreSQL database via Drizzle ORM
- 🎨 Tailwind CSS styling

## Tech Stack

- **Framework:** Next.js 16 (App Router)
- **Language:** TypeScript
- **Database:** PostgreSQL
- **ORM:** Drizzle ORM
- **Styling:** Tailwind CSS
- **Auth:** Custom session-based auth (bcrypt + hashed session tokens)

## Prerequisites

- Node.js 20+
- A PostgreSQL database (local or hosted, e.g. [Neon](https://neon.tech), [Supabase](https://supabase.com), or [Railway](https://railway.app))

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/mfarhankhalid/Code_alpha_ecommerce_site/tree/main
cd <code_alpha_ecommerce_site>
```

### 2. Install dependencies

```bash
npm install
```

### 3. Push the database schema

This project uses Drizzle ORM. Push the schema defined in `src/db/schema.ts` to your database:

```bash
npx drizzle-kit push
```

### 4. Run the development server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start the development server |
| `npm run build` | Build the app for production |
| `npm run start` | Start the production server |
| `npm run lint` | Run ESLint |
| `npm run typecheck` | Run the TypeScript compiler in check mode |

## Project Structure

```
src/
├── app/                # Next.js App Router pages & API routes
│   ├── api/             # REST endpoints (auth, orders, products, health)
│   ├── cart/            # Cart page
│   ├── checkout/        # Checkout page
│   ├── login/, register/ # Auth pages
│   ├── product/[slug]/  # Product detail page
│   ├── shop/             # Product listing page
│   └── account/          # Account / order history page
├── components/          # Reusable UI components
├── db/                   # Drizzle schema & database client
└── lib/                  # Auth, catalog, and formatting utilities
```

## Deploying to GitHub

1. Initialize git and push to a new GitHub repository:

   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<mfarhankhalid>/<code_alpha_ecommerce_site>.git
   git push -u origin main
   ```

2. Make sure `.env` is **not** committed — it's already excluded via `.gitignore`.

## Deploying to Production

This app can be deployed to any platform that supports Next.js, such as [Vercel](https://vercel.com) or [Railway](https://railway.app):

1. Push your code to GitHub (see above).
2. Import the repository into your hosting platform.
3. Deploy. Run `npx drizzle-kit push` against your database beforehand (or as part of your deploy step) to ensure the schema is in place.

## Internship Task

This project was built as a task submission for the **CodeAlpha Web Development Internship**, demonstrating skills in:

- Building a full-stack application with a modern React framework (Next.js App Router)
- Designing and implementing a relational database schema (PostgreSQL + Drizzle ORM)
- Implementing secure user authentication (hashed passwords, session cookies)
- Building complete e-commerce flows: browsing → cart → checkout → order confirmation → order history
- Writing clean, typed, maintainable TypeScript code

## Author

Built by **[Muhammad Farhan Khalid]** as part of the CodeAlpha Internship Program.

- GitHub: [@mfarhankhalid](https://github.com/mfarhankhalid)
- LinkedIn: [mfarhankhalid](https://www.linkedin.com/in/farhan-khalid-cs)

## Acknowledgements

- [CodeAlpha](https://www.codealpha.tech/) for the internship opportunity and project guidance

## License

This project is provided as-is for personal or educational use.
