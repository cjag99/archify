# Archify

[![Python](https://img.shields.io/badge/Python-3.13+-blue?logo=python)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.136+-green?logo=fastapi)](https://fastapi.tiangolo.com/)
[![Next.js](https://img.shields.io/badge/Next.js-16-black?logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19-blue?logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?logo=typescript)](https://www.typescriptlang.org/)
[![Supabase](https://img.shields.io/badge/Supabase-2.28+-green?logo=supabase)](https://supabase.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4-skyblue?logo=tailwindcss)](https://tailwindcss.com/)

Archify is a mono-repo for a software architecture design platform. It contains two connected subprojects:

- `archify-backend`: REST API and domain logic in Python.
- `archify-frontend`: Interactive web UI in Next.js.

## What does Archify do?

Archify helps architects and developers:

- create and store software architecture projects.
- design component diagrams, nodes, and relationships.
- manage design patterns and programming languages.
- upload images and assets via Supabase Storage.
- export architecture projects as downloadable code packages.

## Visual stack

| Layer | Technology | Purpose |
|---|---|---|
| Frontend | `Next.js`, `React`, `TypeScript` | Interactive UI, diagram editor, auth, API consumption |
| Graphing | `AntV X6` | Node-based diagram editor and canvas rendering |
| Backend | `FastAPI`, `Python`, `Pydantic` | REST API, request validation, business rules |
| Architecture | Hexagonal Architecture | Clear separation between API, domain and infrastructure |
| Backend services | `Supabase` | PostgreSQL, Auth, Storage, data persistence |

## Repo structure

```text
archify/
├── archify-backend/   # Python API and hexagonal domain
├── archify-frontend/  # Next.js web interface
└── README.md          # Root documentation
```

## Screenshots

The following screenshots show UI pages and dashboard views included in the `public/` folder.

| Screenshot | Preview |
|---|---|
| `Admin.png` | ![Admin](public/Admin.png) |
| `dashboard.png` | ![Dashboard](public/dashboard.png) |
| `Light.png` | ![Light theme](public/Light.png) |
| `login.png` | ![Login](public/login.png) |
| `project.png` | ![Project](public/project.png) |
| `Responsive.png` | ![Responsive](public/Responsive.png) |

## Submodules

### `archify-backend`

Python backend exposing business logic via REST endpoints. It follows Hexagonal Architecture with clear separation between:

- API layer (`app/api`)
- Domain layer (`app/domain`)
- Infrastructure adapters (`app/infrastructure`)

Read more in [archify-backend/README.md](archify-backend/README.md).

### `archify-frontend`

Frontend built with Next.js and Tailwind CSS. It provides an interactive diagramming experience using AntV X6.

Read more in [archify-frontend/README.md](archify-frontend/README.md).

## Run the project

### Backend

1. Change directory to `archify-backend`
2. Ensure Python 3.13+
3. Install dependencies with `uv sync`
4. Set Supabase environment variables
5. Start the server:

```bash
uvicorn app.main:app --reload
```

### Frontend

1. Change directory to `archify-frontend`
2. Install dependencies:

```bash
npm install
```

3. Start the local development server:

```bash
npm run dev
```

4. Open `http://localhost:3000`

## Requirements

- Node.js (LTS recommended)
- Python 3.13+
- Supabase project with Auth, PostgreSQL, and Storage configured

## More info

- `archify-backend/README.md`: Backend documentation.
- `archify-frontend/README.md`: Frontend documentation.
