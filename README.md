# Geeus AI — Full Stack

Full-stack AI application combining **Clone** (React frontend) and **CreatorApp24** (Python backend) into a unified production repository.

**Repository:** https://github.com/ashleygeeeeg/Geeus-AI

---

## Architecture

```
Geeus-AI/
├── frontend/          # React 19 + Tailwind (from Clone)
│   ├── package.json
│   ├── src/
│   └── public/
├── backend/           # FastAPI + MongoDB (from CreatorApp24)
│   ├── server.py
│   ├── requirements.txt
│   └── models/
├── docker-compose.yml # API + MongoDB orchestration
└── docs/              # Architecture & integration guides
```

### Tech Stack

| Layer | Tech | Source |
|-------|------|--------|
| Frontend | React 19, CRA + Craco, Tailwind, shadcn/Radix, React Router | Clone |
| Backend | FastAPI, Python, MongoDB | CreatorApp24 |
| Infra | Docker Compose | Both |
| Mobile | AppCreator24 (WebView shell) | CreatorApp24 |

---

## Features

### Frontend (Clone)
- Landing page with showcase, features, stats
- Waitlist signup (`POST /api/waitlist`)
- Authentication (signup, login, `/api/auth/me`)
- Dashboard with builds & mock billing
- AI Chat integration (`/api/chat`)
- Routes: `/`, `/auth`, `/dashboard`, `/chat`

### Backend (CreatorApp24)
- FastAPI REST API
- JWT authentication
- MongoDB integration
- AI chat endpoints
- AppMaker24 Android shell integration
- Production-ready architecture

---

## Quick Start (Local)

### Prerequisites
- Docker & Docker Compose
- Node.js 18+ (for local frontend development)
- Python 3.9+ (for local backend development)

### Using Docker Compose

```bash
# Copy environment files
cp .env.example .env
cp frontend/.env.example frontend/.env.local

# Start API + MongoDB
docker compose up --build

# In another terminal, start frontend dev server
cd frontend
yarn install
yarn start
```

Frontend: http://localhost:3000
API: http://localhost:8000
API Docs: http://localhost:8000/docs

---

## Environment Variables

### Root `.env` (Backend)
See `.env.example`:
```
MONGODB_URI=mongodb://mongo:27017/geeus
JWT_SECRET=your-secret-key
EMERGENT_API_KEY=your-api-key
```

### Frontend `frontend/.env.local`
See `frontend/.env.example`:
```
REACT_APP_API_URL=http://localhost:8000
REACT_APP_WEB_URL=http://localhost:3000
```

---

## API Overview

See [`contracts.md`](./contracts.md) for full API specification.

### Key Endpoints
- `POST /api/auth/signup` — Register account
- `POST /api/auth/login` — Login
- `GET /api/auth/me` — Current user
- `POST /api/waitlist` — Add to waitlist
- `POST /api/chat` — Send chat message
- `GET /api/integrations/appmaker24` — AppMaker24 URLs

---

## Deployment

### Frontend (Vercel)
```bash
cd frontend
vercel deploy
```
Configure root directory: `frontend`

### Backend (Docker / Railway / Render)
```bash
docker build -t geeus-api .
docker run -p 8000:8000 geeus-api
```

### AppCreator24 Integration
1. Deploy frontend to Vercel
2. Set environment variables in backend:
   - `PUBLIC_WEB_URL` → Vercel URL
   - `PUBLIC_API_URL` → API URL
   - `APPCREATOR24_APP_URL` → AppCreator24 instance
3. Add WebView menus in AppCreator24 UI
4. Query `GET /api/integrations/appmaker24` for menu URLs

Full guide: [`docs/APPMAKER24.md`](./docs/APPMAKER24.md)

---

## Documentation

- [`docs/ARCHITECTURE.md`](./docs/ARCHITECTURE.md) — Production layout
- [`docs/APPMAKER24.md`](./docs/APPMAKER24.md) — AppCreator24 WebView integration
- [`contracts.md`](./contracts.md) — API contracts & endpoints
- [`CONTRIBUTING.md`](./CONTRIBUTING.md) — Development guidelines

---

## Source Repositories

- **Clone (Frontend):** https://github.com/ashleygeeeeg/Clone
- **CreatorApp24 (Backend):** https://github.com/ashleygeeeeg/creatorapp24

---

## Roadmap

- [ ] Self-hosting guide
- [ ] Plugin system
- [ ] Admin dashboard
- [ ] Multi-tenant support

See [Issues](https://github.com/ashleygeeeeg/Geeus-AI/issues) for full roadmap.

---

## License

MIT — See LICENSE file
