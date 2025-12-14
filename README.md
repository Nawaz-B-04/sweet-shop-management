## Sweet Shop Management System

### Objective
Design, build, and test a full-stack Sweet Shop Management System. This project demonstrates skills in API development, database management, frontend implementation, testing, and modern workflows with AI-assisted coding.

---

### Core Requirements

#### Backend API
- Node.js + Express.js
- PostgreSQL (ORM: Prisma/TypeORM/Sequelize)
- JWT-based authentication (User/Admin)
- Endpoints:
  - `POST /api/auth/register` – Register
  - `POST /api/auth/login` – Login
  - `POST /api/sweets` – Add sweet (Admin)
  - `GET /api/sweets` – List sweets
  - `GET /api/sweets/search` – Search sweets
  - `PUT /api/sweets/:id` – Update sweet (Admin)
  - `DELETE /api/sweets/:id` – Delete sweet (Admin)
  - `POST /api/sweets/:id/purchase` – Purchase sweet
  - `POST /api/sweets/:id/restock` – Restock sweet (Admin)
- Sweet model: ID, name, category, price, quantity

#### Frontend Application
- React.js (Vite), TypeScript, Tailwind CSS / Material UI
- Features:
  - Registration & login forms
  - Dashboard/homepage for sweets
  - Search & filter sweets
  - Purchase button (disabled if out of stock)
  - Admin panel for add/update/delete sweets
- Responsive, modern UI

### Setup Instructions

#### Backend
```sh
cd backend
npm install
npm run dev
```
Set up `.env` in `/backend`:
```
DATABASE_URL=postgresql://user:password@localhost:5432/sweetshop
JWT_SECRET=your_secret_key
PORT=5000
```
Run migrations (if using Prisma/TypeORM):
```sh
npx prisma migrate dev
```
Run tests:
```sh
npm run test
```

#### Frontend
```sh
cd frontend
npm install
npm run dev
```
Set up `.env` in `/frontend`:
```
VITE_API_URL=http://localhost:5000/api
```

---

### Testing
- Backend: Jest + Supertest
```sh
cd backend
npm run test
```

---

## My AI Usage

AI tools were used as development assistants during the implementation of this project, in alignment with Incubyte’s AI usage policy.

### AI Tools Used
- **GitHub Copilot** – Used to generate initial boilerplate code for controllers, services, and DTOs.
- **ChatGPT** – Used to brainstorm API endpoint designs, data models, test cases, and to debug failing tests.
- **Gemini** – Used to review API documentation structure and suggest improvements in naming and consistency.

### How I Used AI
- Generated initial service and controller templates to speed up development.
- Brainstormed edge cases and test scenarios while following Test-Driven Development (TDD).
- Debugged logical errors and test failures by validating assumptions and flows.
- Improved documentation clarity and structure in the README.

### My Reflection on AI Usage
Using AI significantly improved my development workflow by reducing time spent on repetitive boilerplate and helping me think through edge cases more effectively. It allowed me to focus more on core business logic, system design, and code quality.  

All AI-generated suggestions were critically reviewed, modified, and tested manually. Final implementation decisions, architectural choices, and responsibility for correctness remained entirely mine. AI served strictly as a productivity and learning aid, not a replacement for engineering judgment.

---



