# Movie Search + Favorites

A small demo project with a NestJS backend and a Next.js frontend.

---

## What it does

- Search for movies via the OMDb API (by title).
- Add/remove movies from a favorites list.
- Favorites are stored in memory (reset on server restart).
- Swagger/OpenAPI docs are available from the backend.
- The frontend uses TanStack Query for fetching/caching.
- Orval was used to generate a typed API client for the frontend.

## Where did I use AI?

- GitHub Copilot for code completion
- ChatGPT for researching while developing
- Generate a mockup of how the UI should look

## Instructions

- Port 5000 is used for the server, and port 3000 for the front-end.
- Swagger UI is available at: http://localhost:5000/documentation

More information about how to run the projects are avaiable in the `frontend/README.md` and `backend/README.md` files.

## Deployment

### Approach

- Use Docker to containerize both frontend and backend.
- Deploy to a simple VM (AWS EC2, DigitalOcean, etc.) or similar environment.
- Automate deployment with GitHub Actions (SSH into the server and pull/run containers).
- Keep deploy keys and environment variables stored securely in GitHub Secrets.
- Serve the frontend as a bundled static build, either from the same container or via CDN/reverse proxy.

### Things I'd Improve Before Production

- Add better error handling (client and server).
- Expose a `/health` endpoint for monitoring.
- Always serve over HTTPS (via reverse proxy like Nginx or Traefik).
- Configure CORS properly for production.
- Add lazy loading for movie posters and long lists.
- Add unit tests for both frontend and backend.
- Make the Orval-generated base URL configurable for different environments.
- Handle missing posters gracefully (fallback image or filter them out).
- Refactor the search bar into a reusable component.

