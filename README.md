# Sanchalana 2K26 - College Fest Website

A full-stack web application for Sanchalana 2K26, a college cultural and technical fest. Built with the MERN stack.

## Tech Stack

**Frontend**
- React 18 + TypeScript
- Vite (build tool & dev server)
- Tailwind CSS + shadcn-ui (UI components)
- React Router DOM (client-side routing)
- TanStack React Query (server state management)
- Framer Motion (animations)
- Spline (3D interactive elements)

**Backend**
- Node.js + Express.js
- MongoDB + Mongoose (ODM)
- JWT (JSON Web Tokens) for authentication
- bcrypt.js for password hashing

## Getting Started

### Prerequisites
- Node.js >= 18
- MongoDB running locally or a MongoDB Atlas URI

### 1. Clone the repository
```sh
git clone <YOUR_GIT_URL>
cd retroflow-studio
```

### 2. Install dependencies
```sh
npm install
```

### 3. Set up environment variables
Create a `.env` file in the root with:
```
VITE_MONGODB_URI=mongodb://localhost:27017/sanchalana2k26
VITE_JWT_SECRET=your-super-secret-jwt-key
```

### 4. Start the backend server
```sh
node server.js
```
> Runs on http://localhost:5000

### 5. Start the frontend dev server
```sh
npm run dev
```
> Runs on http://localhost:8080

## Project Structure

```
src/
├── components/       # Reusable UI components (HeroSection, Footer, etc.)
├── contexts/         # React Context (AuthContext for global auth state)
├── hooks/            # Custom React hooks
├── lib/              # Utility functions
├── models/           # Mongoose models (if used on frontend)
├── pages/            # Route-level page components
│   ├── Index.tsx
│   ├── Events.tsx
│   ├── Gallery.tsx
│   ├── Team.tsx
│   ├── Scoreboard.tsx
│   ├── Announcements.tsx
│   ├── Contact.tsx
│   ├── About.tsx
│   ├── Login.tsx
│   └── Register.tsx
└── App.tsx           # Root component with routing setup
server.js             # Express backend (auth API + MongoDB)
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Login and receive a JWT |
| GET | `/api/auth/me` | Get logged-in user details (protected) |

## Build for Production
```sh
npm run build
```
