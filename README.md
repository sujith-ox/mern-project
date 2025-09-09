Jobify App

Full‑stack job tracking app with secure auth, job CRUD, filters/sort/pagination, profile with avatar upload, admin stats, and dark mode.
Live Demo

    https://mern-project-4osi.onrender.com/

Stack

    Frontend: React (Vite), React Router v6.10, Styled Components, React Query, Recharts, React Toastify, Axios

    Backend: Node.js, Express, MongoDB, Mongoose, JWT (HTTP‑only cookie), bcryptjs, multer, Cloudinary, express‑validator

    Security: helmet, express‑mongo‑sanitize, express‑rate‑limit

Features

    Register/Login/Logout with hashed passwords and JWT cookies

    First user as admin; role‑based access

    Jobs CRUD with status/type/location

    Search, filter, sort, and paginate jobs

    Profile edit with avatar upload (Cloudinary) and cleanup

    Admin: users/jobs counts

    Dark/light theme with persistence

    React Router loaders/actions + React Query caching and invalidations

    Centralized validation and error handling, axios interceptor auto‑logout

Getting Started

    Clone and env

bash
git clone <your-repo-url>
cd jobify

Create .env (root):

text
PORT=5100
NODE_ENV=development
MONGO_URL=<your-mongodb-connection-string>
JWT_SECRET=<your-jwt-secret>
JWT_EXPIRES_IN=1d
CLOUD_NAME=<cloudinary-cloud-name>
CLOUD_API_KEY=<cloudinary-api-key>
CLOUD_API_SECRET=<cloudinary-api-secret>

    Install

bash
npm run setup-project

    Dev

bash
npm run dev

    API: http://localhost:5100

    Web: http://localhost:5173 (proxy to API)

Scripts

    setup-project: install root + client

    dev: run API and client concurrently

    server / client: run each separately

    setup-production-app: install + build client for server hosting

API Routes

    Auth: POST /auth/register, POST /auth/login, GET /auth/logout

    Users: GET /users/current-user, PATCH /users/update-user, GET /users/admin/app-stats

    Jobs: GET /jobs (query: search, jobStatus, jobType, sort, page, limit), POST /jobs, GET /jobs/:id, PATCH /jobs/:id, DELETE /jobs/:id, GET /jobs/stats

Build/Deploy

    Local: cd client && npm run build, serve build from Express

    Render: use “setup-production-app” to build client; serve ./client/dist from Express

License

MIT
