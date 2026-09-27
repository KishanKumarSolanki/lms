# LMS MERN App

This workspace contains a Vite React client and an Express/Mongoose server.

## First-time setup

1. In MongoDB Atlas, add your current IP address under **Network Access**. For local-only development, Atlas also supports `0.0.0.0/0`, but a specific IP is safer.
2. Copy `server/.env.example` to `server/.env` and set `MONGO_URI` and a private `JWT_SECRET`.
3. Seed the demo users and starter courses:

```powershell
cd server
npm run seed
```

4. Start the API:

```powershell
cd server
npm run dev
```

5. In a second terminal, start the client:

```powershell
cd Client
npm run dev
```

The Vite client proxies `/api` requests to `http://localhost:5000`.

## Demo accounts

- Admin: `admin@lms.com` / `admin123`
- Teacher: `teacher@lms.com` / `teacher123`
- Student: `student@lms.com` / `student123`

Change these credentials before deploying. The client login and registration forms now use the Express API and JWT tokens. Public course endpoints are available at `/api/courses` and `/api/courses/:id`.
