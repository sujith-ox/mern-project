### Jobify App

A full-stack MERN application for job search and tracking, featuring robust authentication, comprehensive job management, and an administrative dashboard.

🔗 **Live Demo:** [Jobify App](https://mern-project-4osi.onrender.com/)

-----

### 🚀 Tech Stack

This application is built using the MERN stack with modern libraries and a focus on security, performance, and user experience.

#### **Frontend**

  * **React (Vite):** A fast, modern frontend framework with Vite for a superior development experience.
  * **React Router v6.10:** Handles client-side routing for a seamless single-page application experience.
  * **Styled Components:** Manages component-level styling and theme toggling.
  * **React Query:** Manages server state, caching, and background data synchronization.
  * **Recharts:** Creates dynamic and responsive charts for the admin dashboard.
  * **React Toastify:** Provides elegant and customizable notifications.
  * **Axios:** A promise-based HTTP client for making API requests.

#### **Backend**

  * **Node.js & Express:** The runtime and web framework for the backend API.
  * **MongoDB & Mongoose:** A NoSQL database and an elegant object data modeling tool.
  * **JWT (HTTP-only cookie):** Secures authentication with JSON Web Tokens.
  * **bcryptjs:** Handles password hashing for robust security.
  * **multer & Cloudinary:** Manages file uploads and stores user avatars in the cloud.
  * **express-validator:** A robust middleware for server-side data validation.

#### **Security & Performance**

  * **Helmet:** Secures Express apps by setting various HTTP headers.
  * **express-mongo-sanitize:** Prevents MongoDB injection attacks.
  * **express-rate-limit:** Protects against brute-force and DDoS attacks.
  * **Axios Interceptors:** Implements automatic logout on 401 Unauthorized responses.

-----

### ✨ Key Features

  * **Authentication:** Secure user registration, login, and logout with hashed passwords and JWTs stored in HTTP-only cookies.
  * **Authorization:** First user is designated as an admin, providing role-based access control.
  * **Job Management:** Full CRUD (Create, Read, Update, Delete) functionality for managing jobs, including status, type, and location.
  * **Job Search & Filtering:** Powerful search, filtering, sorting, and pagination options to easily find jobs.
  * **User Profile:** Edit user information and upload/update a profile avatar using Cloudinary.
  * **Admin Dashboard:** View application statistics, including user and job counts.
  * **Theming:** Persistent dark/light mode for a personalized user experience.
  * **Optimized Performance:** Leverages React Router loaders/actions for efficient data fetching and React Query for intelligent caching.
  * **Robust Error Handling:** Centralized validation and error handling for a smoother user experience.

-----

### ⚙️ Getting Started

Follow these steps to set up and run the project locally.

#### **1. Clone the repository**

```bash
git clone <https://github.com/sujith-ox/mern-project/tree/main>
cd jobify
```

#### **2. Setup Environment Variables**

Create a `.env` file in the root directory and add the following variables:

```
PORT=5100
NODE_ENV=development
MONGO_URL=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRES_IN=1d
CLOUD_NAME=your_cloudinary_cloud_name
CLOUD_API_KEY=your_cloudinary_api_key
CLOUD_API_SECRET=your_cloudinary_api_secret
```

#### **3. Install Dependencies**

```bash
npm run setup-project
```

#### **4. Run the Application**

```bash
npm run dev
```

The application will run with the backend API on `http://localhost:5100` and the frontend on `http://localhost:5173`.

-----

### 🔌 API Endpoints

A quick overview of the main API routes available.

| **Endpoint** | **Method** | **Description** |
| :--- | :--- | :--- |
| `/api/v1/auth/register` | `POST` | Registers a new user |
| `/api/v1/auth/login` | `POST` | Logs in a user |
| `/api/v1/auth/logout` | `GET` | Logs out the current user |
| `/api/v1/jobs` | `GET` | Retrieves all jobs with optional queries |
| `/api/v1/jobs` | `POST` | Creates a new job |
| `/api/v1/jobs/:id` | `GET` | Retrieves a single job by ID |
| `/api/v1/jobs/:id` | `PATCH` | Updates a job by ID |
| `/api/v1/jobs/:id` | `DELETE` | Deletes a job by ID |
| `/api/v1/jobs/stats` | `GET` | Provides monthly job application stats |
| `/api/v1/users/current-user`| `GET` | Gets the authenticated user's data |
| `/api/v1/users/update-user`| `PATCH`| Updates the current user's data |
| `/api/v1/users/admin/app-stats`| `GET`| Admin-only endpoint for app stats |

-----

### 🚀 Deployment

#### **Local Production Build**

You can serve the frontend from the Express server.

1.  Navigate into the `client` directory: `cd client`
2.  Build the client: `npm run build`
3.  The server will automatically serve the `/client/dist` directory.

#### **Render (or similar PaaS)**

The project includes a script to prepare for production deployment.

```bash
npm run setup-production-app
```

This command installs dependencies, builds the client, and sets up the server to serve the static files, making it ready for deployment on platforms like Render.

### 📄 License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
