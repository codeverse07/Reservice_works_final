# Reservice_works_final
This repository is my final work of this project that i have completed and We are still working on this to make this project a complete success and ready to be deployed live in upcoming days.

# Reservice
Reservice is a comprehensive full-stack web application designed for managing service bookings, technicians, and administrators. It features real-time notifications, a robust booking lifecycle, and dedicated dashboards for Users, Technicians, and Super Admins.
## Features
- **User Dashboard**: Browse services, book appointments, and manage your booking history.
- **Technician Dashboard**: View assigned jobs, manage real-time job statuses (Pending, In Progress, Checked-in, Completed), and get sound-enabled real-time notifications for new arrivals.
- **Super Admin Dashboard**: Centralized management of users, technicians, and real-time monitoring of all platform bookings.
- **Booking Lifecycle Management**: Real-time status tracking from generation to completion or cancellation.
- **Real-time Notifications**: Socket.IO integration for instant alerts and updates across all roles.
- **Authentication**: JWT-based secure authentication with Google OAuth integration.
- **Media Management**: Cloudinary integration for image uploads and management.
## Tech Stack
### Frontend
- React 19 / Vite
- Tailwind CSS
- Framer Motion & GSAP (for animations)
- React Router DOM
- React Query (for state & data fetching)
- Socket.IO Client
- Headless UI
### Backend
- Node.js / Express
- MongoDB with Mongoose
- Socket.IO (for real-time features)
- Passport (Google OAuth2.0) & JWT
- Cloudinary & Multer
- Joi (for payload validation)
- Morgan & Helmet (for security and logging)
## Project Structure
```
.
├── frontend             # React/Vite Frontend Application
│   ├── src              # Source code (components, pages, context, etc.)
│   └── package.json     # Frontend dependencies
├── backend              # Node/Express Backend Application
│   ├── src              # Server source code (controllers, routes, models, etc.)
│   └── package.json     # Backend dependencies
└── package.json         # Root package manager for concurrent execution
```
## Getting Started
### Prerequisites
- Node.js (v18+ recommended)
- MongoDB running locally or a valid MongoDB URI
- Cloudinary Account (for media uploads)
- Google OAuth Credentials (for Google login)
### Installation
1. **Clone the repository:**
   ```bash
   git clone <your-repo-url>
   cd reservice
   ```
2. **Install all dependencies** (Frontend & Backend):
   ```bash
   npm run install:all
   ```
3. **Set up environment variables:**
   - Navigate to `backend` and create a `.env` file based on `.env.example`.
   - Update `frontend/.env` with required Vite environment variables (like Socket URL and API endpoints).
4. **Run the application (Development Mode):**
   Run both frontend and backend concurrently from the root directory:
   ```bash
   npm run start
   ```
   Alternatively, you can run them separately using the root scripts:
   ```bash
   # Run Backend
   npm run dev:backend
   # Run Frontend (User App)
   npm run dev:frontend
   ```
## Production Build
To build the frontend for production:
```bash
npm run build:frontend
```
This will compile the frontend assets into the respective `dist-*` directories for serving via the backend or a CDN. Production builds for `USER` and `TECH` apps can be triggered via `build:user` and `build:tech` scripts in the `frontend` folder.
## License
This project is licensed under the ISC License.
