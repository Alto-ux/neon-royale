# NEON ROYALE — Online Arcade

Score-only fictional arcade platform. No money, deposits, withdrawals, or monetary prizes.

## Local

```powershell
npm install
$env:ADMIN_USER="admin"
$env:ADMIN_PASSWORD="change-this-password"
$env:SESSION_SECRET="use-a-long-random-secret"
npm start
```

Open `http://localhost:3000` and admin at `http://localhost:3000/admin`.

## Online with Render

1. Upload the project to GitHub.
2. In Render create **New → Web Service** and connect the GitHub repo.
3. Build command: `npm install`
4. Start command: `npm start`
5. Set environment variables: `NODE_ENV=production`, `ADMIN_USER`, `ADMIN_PASSWORD`, `SESSION_SECRET`, `DATA_DIR=/var/data`.
6. For SQLite persistence, attach a persistent disk mounted at `/var/data`. Without persistent storage, local database files can be lost on restarts/redeploys.

After deploy, use the Render URL for both the player site and `/admin`.
