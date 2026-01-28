# Example: Task Management App

Contoh output lengkap dari solo-dev workflow untuk membangun aplikasi Task Management sederhana.

## 01-brainstorm-output.md

Hasil dari Brainstorming Agent:

### Context
Eksplorasi ide untuk membangun task management app yang simple dan fast untuk personal use.

### Problem Space
- Aplikasi task management existing terlalu kompleks
- Butuh waktu lama untuk add simple task
- Terlalu banyak fitur yang tidak terpakai

### Target Users
Individual users yang ingin organize daily tasks dengan cepat tanpa overwhelmed dengan fitur.

### Ideas Generated

#### High Priority
1. **Quick Add Task** - Add task dalam < 5 detik dengan minimal input
2. **Simple Status Toggle** - TODO → IN_PROGRESS → DONE dengan satu klik
3. **Due Date Reminder** - Optional due date dengan visual indicator

#### Medium Priority
1. **Priority Levels** - Low/Medium/High untuk sorting
2. **Search & Filter** - Find tasks by keyword or status

### Technical Considerations

**Preferred Tech Stack:**
- Frontend: React (familiar), TypeScript
- Backend: Node.js (JavaScript full-stack)
- Database: PostgreSQL (structured data)

**Infrastructure Constraints:**
- Hosting: Free tier only (Vercel + Railway)
- Budget: $0/month
- Deployment: Simple deployment preferred

**Performance Requirements:**
- Response Time: < 2 seconds page load
- Concurrent Users: 1 user (personal use)

**Developer Constraints:**
- Experience Level: Comfortable with React, basic backend knowledge
- Time Constraint: Want MVP in 2-3 weeks
- Team Size: Solo developer

---

## 02-rapid-prd-output.md

Hasil dari Rapid PRD Agent (simplified - hanya bagian penting):

### Functional Requirements

#### Must Have (P0)
| ID | Requirement | Acceptance Criteria |
|----|-------------|---------------------|
| FR-01 | User can register account | Email validation, password min 8 chars |
| FR-02 | User can login | Email + password auth, session 7 days |
| FR-03 | User can create task | Title required, description optional, default status TODO |
| FR-04 | User can view task list | See all tasks, sorted by created date |
| FR-05 | User can update task status | Toggle between TODO/IN_PROGRESS/DONE |
| FR-06 | User can delete task | Confirmation dialog before delete |

### Tech Stack Decision

**Frontend:** React 18 + TypeScript + Vite + Tailwind CSS
**Backend:** Node.js + Express + Prisma
**Database:** PostgreSQL
**Hosting:** Vercel (frontend) + Railway (backend)

### Data Model

```
User (id, email, passwordHash, createdAt)
  ↓ 1:N
Task (id, userId, title, description, status, priority, dueDate, createdAt)
```

---

## 03-technical-breakdown-output.md

Hasil dari Technical Breakdown Agent (simplified - hanya 3 tasks pertama):

### Part 1: Code Foundation

#### Project Structure
```
task-app/
├── frontend/src/
│   ├── components/
│   │   ├── auth/ (LoginForm, RegisterForm)
│   │   ├── tasks/ (TaskList, TaskItem, TaskForm)
│   │   └── shared/ (Button, Input, Modal)
│   ├── services/ (api.ts, auth.service.ts, task.service.ts)
│   └── types/ (user.ts, task.ts)
└── backend/src/
    ├── routes/ (auth.routes.ts, task.routes.ts)
    ├── controllers/
    ├── services/
    └── middleware/ (auth.middleware.ts)
```

#### Code Conventions
- Components: PascalCase (TaskList.tsx)
- Functions: camelCase (createTask)
- Constants: UPPER_SNAKE_CASE (API_BASE_URL)

---

### Part 2: Development Tasks

#### Epic 1: Project Setup (5 tasks)

**Task 1.1: Initialize Project**
- [ ] Create monorepo structure
- [ ] Initialize React + Vite + TypeScript
- [ ] Initialize Node.js + Express backend
- **Files:** package.json, tsconfig.json, vite.config.ts

**Task 1.2: Setup Database**
- [ ] Install Prisma
- [ ] Create User model
- [ ] Run migrations
- **Files:** prisma/schema.prisma

---

#### Epic 2: Authentication (8 tasks)

**Task 2.1: Create User Model**
- [ ] Define User schema in Prisma
- [ ] Create migration
- **Files:** prisma/schema.prisma, migrations/001_create_users.sql

**Task 2.2: Implement Registration API**
- [ ] POST /api/v1/auth/register
- [ ] Email validation
- [ ] Password hashing
- **Files:** routes/auth.routes.ts, controllers/auth.controller.ts, services/auth.service.ts

---

#### Epic 3: Task Management (6 tasks)

**Task 3.1: Create Task Model**
**Task 3.2: Implement Task CRUD APIs**
**Task 3.3: Create Task List UI**
...

---

### Part 3: Implementation Roadmap

**Week 1:** Epic 1 (Setup) + Epic 2 (Auth Backend)
**Week 2:** Epic 2 (Auth Frontend) + Epic 3 (Task Backend)
**Week 3:** Epic 3 (Task Frontend) + Deployment

**Total:** 19 tasks across 4 epics

---

## Next: Implement with Superpowers

```bash
# Copy Epic 2 tasks to TodoWrite
# Then use superpowers skills:

/brainstorm    # Explore auth implementation approach
/tdd           # Implement auth with TDD
/verification  # Verify all tests pass
/code-review   # Review before merge
```

---

**This example shows the complete flow from brainstorming → actionable technical tasks ready for implementation!**
