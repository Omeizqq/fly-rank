# CLAUDE Rules and Conventions

## Purpose
This file documents the stack, architecture, coding conventions, and operational notes for the **Buy Wrap** project.

## Stack Overview
- **Frontend:** JavaScript
- **Backend:** Node.js
- **Database:** PostgreSQL
- **Other Tools:** Bootstrap for styling, Docker + docker-compose for containerization

## Repo Layout
- `/frontend` — JavaScript frontend application
- `/backend` — Node.js backend API
- `/db` — Database migrations and seed scripts
- `/docs` — Design documents and diagrams
- `/scripts` — Helper scripts

## Branching and Releases
- `main` — production-ready, protected branch
- Feature branches: `feat/<short-desc>`
- Pull Requests must include a description, linked issue, and pass CI checks

## Coding Conventions
- **Language:** JavaScript (ES6+)
- **Formatting:** Prettier default config
- **Linting:** ESLint with recommended rules
- **Commit messages:** Conventional Commits (e.g., `feat: add checkout flow`)
- **Tests:** Jest for unit tests; integration tests in `/tests`

## Environment and Secrets
- Use `.env.example` to list required variables
- Never commit `.env` or secrets
- For local development, use `docker-compose` to run PostgreSQL and services

## Running Locally
1. Copy `.env.example` to `.env` and fill in values
2. Run `docker-compose up --build`
3. Install dependencies:
   ```bash
   cd frontend && npm install
   cd ../backend && npm install
