🐐 LOTI Notes — AI-Powered Notes App
An AI-powered note-taking web app built with Next.js 15 and the OpenAI API. Users can sign up, log in, write and organize personal notes, and ask an AI assistant questions about their own notes — the AI reads through your notes and answers based on their content.
✨ What It Does
📝 Create, edit, and delete notes — a simple, distraction-free note editor with autosave.
🔐 User authentication — sign up / log in / log out, with each user's notes kept private and tied to their account.
🤖 Ask AI about your notes — chat with an AI assistant (powered by OpenAI's `gpt-4o-mini`) that reads all of your notes and answers questions about them, with support for multi-turn conversation.
🌗 Dark mode — toggle between light and dark themes.
📱 Responsive sidebar UI — browse and switch between notes from a collapsible sidebar, built with accessible, pre-styled UI components (Radix UI + shadcn/ui).
🔍 Fast client-side note search powered by Fuse.js.
🧱 Tech Stack
Layer	Technology
Language	TypeScript
Framework	Next.js 15 (App Router, React 19)
Styling	Tailwind CSS + shadcn/ui + Radix UI primitives
Database	PostgreSQL
ORM	Prisma
Authentication	Supabase Auth
AI	OpenAI API (`gpt-4o-mini`)
Package manager	pnpm
Primary programming language: TypeScript (React/JSX components, Next.js server actions and API routes), styled with Tailwind CSS and backed by a PostgreSQL database via Prisma.
📂 Project Structure
```
my-app/
├── src/
│   ├── app/              # Next.js App Router pages & API routes (login, sign-up, home)
│   ├── actions/          # Server actions (notes CRUD, AI question-answering, user auth)
│   ├── auth/              # Supabase auth server helper
│   ├── components/        # React UI components (sidebar, note editor, buttons, dialogs, etc.)
│   ├── components/ui/     # Reusable shadcn/ui primitives
│   ├── db/                 # Prisma schema & migrations
│   ├── hooks/               # Custom React hooks
│   ├── openai/              # OpenAI client configuration
│   ├── providers/           # React context providers (notes, theme)
│   └── styles/               # Global and AI-response CSS
└── package.json
```
🗄️ Data Model
The app uses two core Prisma models:
User — id, email, and their notes.
Note — id, text content, author, and timestamps.
🚀 Getting Started
Prerequisites
Node.js
pnpm
A PostgreSQL database
A Supabase project (for auth)
An OpenAI API key
Setup
Clone the repository and install dependencies:
```bash
   cd my-app
   pnpm install
   ```
Create a `.env.local` file with the following variables:
```
   DATABASE_URL=your_postgres_connection_string
   SUPABASE_URL=your_supabase_url
   SUPABASE_ANON_KEY=your_supabase_anon_key
   OPENAI_API_KEY=your_openai_api_key
   ```
Run database migrations:
```bash
   pnpm migrate
   ```
Start the development server:
```bash
   pnpm dev
   ```
Open http://localhost:3000 in your browser.
📜 Available Scripts
Command	Description
`pnpm dev`	Run the app in development mode (with Turbopack)
`pnpm build`	Generate the Prisma client and build for production
`pnpm start`	Start the production server
`pnpm lint`	Run ESLint
`pnpm migrate`	Generate the Prisma client and run database migrations
📄 License
No license file was included in this project. Add one if you plan to distribute or open-source it.

