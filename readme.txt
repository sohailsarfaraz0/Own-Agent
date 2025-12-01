7) Example docker-compose usage
docker compose up --build
# open http://localhost:3000

8) .env and port config notes

Frontend uses NEXT_PUBLIC_API_URL in .env.local — that will be available in client-side code.

Backend uses .env for host/port/CORS allowed origins.

For production, never expose sensitive secrets in .env to the client. Keep server secrets server-side and inject at runtime.

9) Sample code recap
FastAPI endpoint — /api/v1/hello

(See earlier hello.py)

Next.js page — fetch process.env.NEXT_PUBLIC_API_URL + "/hello"

(See earlier pages/index.js)