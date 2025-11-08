# Next.js 14 Dashboard Project

This is a full-stack dashboard application built by following the official [Next.js Learn Course](https://nextjs.org/learn) by Vercel. It's a comprehensive project that demonstrates the core features of the Next.js App Router, including data fetching, authentication, form handling, and more.

The application includes a public landing page, a login page, and a protected dashboard area. The dashboard allows users to manage customers and invoices (full CRUD functionality) and view an overview page with revenue charts and summary statistics.

## Key Features

  * **Full-Stack Framework:** Built with **Next.js 14** using the **App Router** paradigm.
  * **Authentication & Authorization:** Implements secure credential-based login (email/password) using **NextAuth.js (v5)**. Protected routes are enforced using Next.js Middleware.
  * **Database Integration:** Connects to a **PostgreSQL** database (via `postgres.js`) for all data fetching and mutations.
  * **Server Components & Actions:** Leverages **Server Components** for efficient, server-side data fetching and **Server Actions** for secure, server-side form handling and mutations (Create, Update, Delete).
  * **UI Streaming & Skeletons:** Uses **React Suspense** and custom loading skeletons (`skeletons.tsx`) to stream UI components as data becomes available, improving perceived performance and user experience.
  * **Advanced Form Validation:** Employs **Zod** for schema-based server-side validation and uses the `useActionState` hook to display errors directly in the form components.
  * **Search & Pagination:** Implements server-side search and pagination, with state managed entirely through **URL Search Params**.
  * **Styling:** Fully responsive design built with **Tailwind CSS**.
  * **Error Handling:** Features robust error handling using Next.js file-based conventions like `error.tsx` and `not-found.tsx`/edit/not-found.tsx\`].
  * **Metadata:** Implements dynamic, page-specific metadata for SEO using the `Metadata` API.

## Installation and Usage

To run this project locally, you will need `pnpm` (based on `pnpm-lock.yaml`) and access to a PostgreSQL database.

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/dusmamud/nextjs-dashboard-learn.git
    cd nextjs-dashboard-learn
    ```

2.  **Install dependencies:**

    ```bash
    pnpm install
    ```

3.  **Set up environment variables:**
    Create a `.env` file in the root of the project (this file is ignored by git). You need to add your PostgreSQL connection string and a secret for NextAuth.js.

    ```.env
    POSTGRES_URL="your_postgresql_connection_string"
    AUTH_SECRET="your_strong_random_secret_for_nextauth"
    ```

4.  **Run the database seed (Optional but Recommended):**
    If you are using the Vercel Postgres template, you can run a seed script (not provided in files, but part of the original course) to populate your database with initial data.

5.  **Run the development server:**

    ```bash
    pnpm run dev
    ```

6.  **Open the application:**
    Open `http://localhost:3000` in your browser.

## Demo Credentials

You can use the following credentials to log in, as specified in the original course:

  * **Email:** `user@nextmail.com`
  * **Password:** `123456`

## Technologies Used

  * **Framework:** Next.js 14 (App Router)
  * **Language:** TypeScript
  * **Authentication:** NextAuth.js (v5)
  * **Database:** PostgreSQL (`postgres.js`)
  * **Styling:** Tailwind CSS
  * **Validation:** Zod
  * **Password Hashing:** bcrypt
  * **UI:** React 19 (latest), Headless UI (`@heroicons/react`)
  * **Utilities:** `clsx`, `use-debounce`

## Author

  * **Name:** Dus Mamud
  * **GitHub:** [dusmamud](https://www.google.com/search?q=https://github.com/dusmamud)

## Acknowledgments

This project is a direct implementation of the official [Next.js Learn Course](https://nextjs.org/learn) from Vercel. All credit for the project structure, design, and learning curriculum goes to the Vercel and Next.js teams.

## License

This project is licensed under the MIT License.
