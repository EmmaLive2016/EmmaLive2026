# Emma Adventure Channel Starter

## What is included
- `frontend/index.html` — single-file frontend with route-style pages, live-page pop-outs, real-time comments (WebSocket + polling fallback), camera preview, uploads, and a browser-only internal lock for prototype use.
- `backend/app/main.py` — FastAPI starter with comments endpoints, journal endpoints, profanity blocking, and a websocket route for live comments.
- `netlify.toml` and `frontend/_redirects` — Netlify config to publish the frontend and proxy `/api/*` to Render.
- `render.yaml` — Render starter manifest.
- Pink/red Emma theme across the live app UI.
- `SECURITY_PLAN.md` — production security checklist.

## Deploy
1. Deploy `frontend/` to Netlify.
2. Deploy `backend/` to Render.
3. Replace `YOUR-RENDER-BACKEND.onrender.com` in `netlify.toml` and `frontend/_redirects`.
4. Optional: set `window.EMMA_BACKEND_ORIGIN` in the frontend if you want direct WebSocket push from a separate backend origin.
5. Set backend environment variables from `.env.example`.

## Routes in the frontend
- `#/home`
- `#/channels`
- `#/live`
- `#/videos`
- `#/shorts`
- `#/photos`
- `#/journal`
- `#/studio/emma`

## Prototype caveat
The HTML file stores uploads and some viewer state locally for demo use. Real multi-user comments, moderation, authentication, and media storage must be enforced by the backend.
