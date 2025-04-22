# Mini Message Board Roadmap

## Tech Stack

### Frontend

- **Framework**: React.js (with TypeScript)
- **Build Tool**: Vite
- **Styling**: Tailwind CSS with shadcn/ui
- **State Management**: Zustand
- **Routing**: React Router
- **HTTP Client**: axios
- **Server State Management**: TanStack Query (React Query)
- **Form Handling**: react-hook-form
- **Animation**: Framer Motion
- **Testing**: Jest + React Testing Library (Optional)

### Backend

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: PostgreSQL
- **ORM**: Prisma
- **Authentication**: JWT (JSON Web Tokens)
- **API**: RESTful
- **Middleware**:
  - `cors`
  - `helmet`
  - `morgan` (for development)
  - `express.json`
  - `express.urlencoded`
  - _(Consider later: `compression`, `express-validator`, `express-rate-limit`)_

## Development Roadmap

### Phase 1: Project Setup

- **Directory Structure**: Create `frontend` and `backend` directories.
- **Initialize Projects**:
  - `frontend`: Use Vite for React + TypeScript setup.
  - `backend`: Use `npm init`.
- **Install Dependencies**: Install chosen libraries/frameworks in respective directories.
- **Basic Folder Structure**: Set up `src` folders and initial subdirectories (components, routes, controllers, db, etc.).
- **Linting & Formatting**: Configure ESLint and Prettier for both projects.

### Phase 2: Backend Development (Node.js/Express/Prisma/PostgreSQL)

- **Server Setup**: Create `backend/server.js`. Integrate middleware (`cors`, `helmet`, `morgan`, `express.json`, `express.urlencoded`).
- **Prisma Setup**: Initialize Prisma, configure PostgreSQL connection, define schema (`schema.prisma` with User and Message models), run initial migration.
- **API Endpoints**: Create Express routes for:
  - `POST /api/auth/register`
  - `POST /api/auth/login`
  - `GET /api/messages`
  - `POST /api/messages` (Protected)
  - _(Optional Later)_ `PUT /api/messages/:id` (Protected)
  - _(Optional Later)_ `DELETE /api/messages/:id` (Protected)
- **Controllers/Service Logic**: Implement logic using Prisma Client for database interactions.
- **Authentication**: Implement JWT generation on login and middleware for verifying tokens on protected routes.
- **Error Handling**: Implement centralized error handling middleware.
- **Validation**: Add basic input validation (e.g., using Prisma or `express-validator`).

### Phase 3: Frontend Development (React/TS/Tailwind/shadcn/Zustand/Axios/TanStack Query/Framer Motion)

- **Project Structure**: Organize `frontend/src` (components, pages, hooks, store, services, etc.).
- **Layout & Routing**: Set up main layout and `React Router` (e.g., Message Board page, Login/Register pages).
- **Component Development**: Build UI using shadcn/ui components (`Card`, `Input`, `Button`, etc.) for message display and forms.
- **State Management (Zustand)**: Create store for UI state, potentially auth token/user info.
- **API Integration**: Create `axios` service functions. Use `TanStack Query` for fetching/caching messages and handling server state.
- **Form Handling**: Use `react-hook-form` for login, registration, and message submission forms.
- **Styling**: Apply Tailwind CSS utility classes.
- **Animation**: Use `Framer Motion` for UI enhancements (e.g., message list animations).
- **Testing (Optional)**: Write tests with Jest & React Testing Library.

### Phase 4: Integration & Testing

- **End-to-End Testing**: Verify full workflow (register, login, post message, view messages).
- **Cross-Browser/Device Check**: Basic testing on different browsers/sizes.
- **Refinement**: Bug fixing, performance checks, code review/refactoring.

### Phase 5: Deployment

- **Backend Prep**: Configure environment variables, production build steps.
- **Backend Host**: Choose & deploy to Railway, Render, Heroku, etc. Set up PostgreSQL instance.
- **Frontend Prep**: Production build (`npm run build`).
- **Frontend Host**: Choose & deploy to Vercel, Netlify, etc. Configure API endpoint URL.
- **CI/CD (Optional)**: Set up automation via GitHub Actions or similar.

### Phase 6: Enhancements (Post-MVP)

- Real-time updates (WebSockets - Socket.IO)
- User Profiles/Avatars
- Message Editing/Deletion
- Message Threading/Replies
- Pagination/Infinite Scrolling
- Advanced UI/UX improvements
