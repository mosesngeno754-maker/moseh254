# Simple Login Web (Node + Express + SQLite)

Quick demo of a minimal login flow with registration, login, session-based auth.

Prerequisites:
- Node 16+
- npm

Install and run:
```bash
# install deps
npm install

# start server
npm start

# dev (auto restart)
npm run dev
```

Open http://localhost:3000/register and create an account.

Security notes:
- The example uses in-memory session store (express-session default). For production, use a persistent session store (Redis, database).
- Set SESSION_SECRET environment variable in production to a strong secret.
- Enable `cookie.secure = true` when serving over HTTPS.
- Rate-limit login attempts and validate/escape inputs more thoroughly in real apps.
- Use HTTPS and consider CSRF protections for forms.