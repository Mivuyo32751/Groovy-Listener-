# Groovy

Groovy is a music discovery and listening demo built with Next.js and React.

## Run from Git Bash

In VS Code, open **Terminal → New Terminal** and select **Git Bash** as the terminal profile. From the project root (`task-manager`), run:

```bash
npm run dev
```

The development server uses port `3000`. Open [http://localhost:3000](http://localhost:3000). Keep the terminal open while Groovy is running. Press `Ctrl+C` in that terminal to stop the server before starting it again.

If Git Bash says port `3000` is already in use, find the process ID and check which app owns it:

```bash
netstat.exe -ano | grep LISTENING | grep ':3000'
tasklist.exe /FI "PID eq 1234"
```

Replace `1234` with the PID from `netstat`. If it is an old Groovy/Node development server, stop it and start Groovy again:

```bash
taskkill.exe //PID 1234 //F
npm run dev
```

Only stop the PID after confirming it is the old Groovy server. The fixed port prevents Next.js from silently switching between `3000`, `3001`, and other addresses.

## Current demo limits

Profiles, Library items, and listening history are currently stored in this browser. Tracks and audio are demo content. See [BACKEND_PLAN.md](./BACKEND_PLAN.md) for the backend build plan.
