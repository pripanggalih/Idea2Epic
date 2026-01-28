# Idea to Epic: Universal AI Workflow untuk Solo Developer

Kumpulan prompt AI untuk mengubah ide menjadi **technical tasks yang actionable** dan siap dikoding. **Language-agnostic** dan **platform-universal** - bekerja untuk Python, Go, Swift, Rust, Java, Kotlin, JavaScript, dan bahasa apapun. Dirancang khusus untuk **solo developer** yang ingin langsung implementasi.

🚀 **Simple, Powerful, Universal, Ready to Code.**

---

## ⚡ Kenapa Workflow Ini?

**Problem:** Epic & Stories dari workflow tradisional masih berupa acceptance criteria. Solo developer masih harus manual breakdown jadi technical tasks.

**Solution:** Workflow ini langsung menghasilkan:
- ✅ Technical tasks dengan file paths spesifik **untuk bahasa/platform apapun**
- ✅ Code standards & conventions **adaptive per language** (Python/Go/Swift/Rust/etc.)
- ✅ Testing strategy & Git workflow **sesuai ecosystem**
- ✅ Platform-aware recommendations (Web/Mobile/CLI/Desktop/API)
- ✅ Format compatible dengan superpowers TodoWrite
- ✅ Direct handoff ke `/tdd`, `/frontend-design`, `/verification`

**Result:** 40% lebih cepat dari workflow tradisional (3 agents vs 5 agents).

---

## 🎯 Workflow Overview

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  Brainstorming  │────▶│   Rapid PRD     │────▶│   Technical     │────▶│  Implementation │
│                 │     │                 │     │   Breakdown     │     │  (Superpowers)  │
└─────────────────┘     └─────────────────┘     └─────────────────┘     └─────────────────┘

Eksplorasi ide +       Requirements +          Code standards +         /brainstorm →
Technical constraints  Tech stack +            Granular tasks +         /tdd →
                      Data model              Superpowers mapping      /verification
```

---

## 🚀 Quick Start

### 1. Pilih Agent Pertama

Salin konten dari `prompts/01-brainstorming-agent.md` ke platform AI pilihan Anda:
- ChatGPT (Custom GPT)
- Claude (Projects)
- Google Gemini (Gems)
- Perplexity AI

### 2. Ikuti Workflow

**Brainstorming** → Eksplorasi ide + **pilih tech stack** (Python/Go/Swift/Rust/Java/JS/etc.)
↓
**Rapid PRD** → Requirements + **tech stack adaptive** + data model (all-in-one)
↓
**Technical Breakdown** → **Language-specific** code foundation + granular tasks
↓
**Implementation** → Gunakan superpowers skills atau code langsung

### 3. Implement dengan Superpowers

```bash
# Copy tasks dari Technical Breakdown ke TodoWrite
# Lalu gunakan superpowers skills:

/brainstorm    # Explore implementation approach
/writing-plans # Create detailed plan
/tdd           # Implement with tests first
/verification  # Verify before completion
/code-review   # Review before merge
```

---

## 📁 Struktur Project

```
Idea2Epic/
├── README.md                          # File ini
│
├── prompts/                           # 3 Agent Prompts
│   ├── 01-brainstorming-agent.md      # Eksplorasi ide + technical constraints
│   ├── 02-rapid-prd-agent.md          # Requirements + Tech stack + Data model
│   └── 03-technical-breakdown-agent.md # Code standards + Granular tasks
│
├── examples/
│   └── task-management-app-example.md # Contoh output lengkap
│
├── docs/
│   └── design-rationale.md            # Penjelasan design decisions
│
└── SETUP-*.md                         # Setup guides
    ├── SETUP-CHATGPT.md
    ├── SETUP-GEMINI.md
    └── SETUP-PERPLEXITY.md
```

---

## 📋 3 Agents Overview

### Agent 1: Brainstorming
**Role:** Creative Facilitator + Technical Advisor

**Input:** Ide awal dari user

**Output:**
- Problem space & target users
- Ideas (prioritized: High/Medium/Low)
- **Project Type** (Web/Mobile/CLI/Desktop/API/Game/Embedded)
- **Tech Stack Preference** (Python/Go/Swift/Rust/Java/Kotlin/JS/etc.)
- **Technical considerations** (platform, deployment, constraints, budget)
- Assumptions & open questions

**Key Feature:** ✨ **Language-agnostic** - tidak assume JavaScript, tanya dulu!

---

### Agent 2: Rapid PRD
**Role:** Product Manager + Software Architect (Hybrid)

**Input:** Brainstorming output

**Output (All-in-One Document):**
- Functional Requirements (Must/Should/Could/Won't)
- Non-Functional Requirements (Performance, Security, etc.)
- **Tech Stack Decision** ✨ **adaptive** per language (Django/Gin/Spring/FastAPI/Express/etc.)
- **High-level Data Model** ✨ **adaptive** per storage (SQL/NoSQL/Core Data/CLI configs/etc.)
- Success metrics

**Key Feature:** Gabungan Product Brief + PRD + Architecture essentials. **Platform-universal.** No redundancy.

---

### Agent 3: Technical Breakdown
**Role:** Lead Developer

**Input:** Rapid PRD

**Output:**
1. **Code Foundation** ✨ **Language-Specific**
   - Project structure **per platform** (Web/Mobile/CLI structure)
   - Code conventions **per language** (PEP 8/Go guidelines/Swift style/etc.)
   - Testing strategy **per ecosystem** (pytest/go test/XCTest/JUnit/etc.)
   - API design patterns **adaptive** (REST/GraphQL/gRPC/CLI commands/etc.)
   - Git workflow (branch naming, commit format)

2. **Development Tasks** (Granular, 1-3 days each)
   - Epic breakdown
   - Task checklist **dengan syntax yang benar**
   - **File paths explicitly specified** (sesuai convention language)
   - Acceptance criteria
   - Dependencies mapped

3. **Implementation Roadmap**
   - Task dependencies
   - Suggested order (MVP first)
   - **Superpowers skill recommendations**
   - Complexity estimates (High/Medium/Low)

**Key Feature:** Bridge dari requirements → actionable code tasks. **Benar untuk Python, Go, Swift, Rust, Java, Kotlin, JavaScript, dll.** TodoWrite compatible.

---

## 💡 Contoh Output

Lihat contoh lengkap untuk **Task Management App**:
- [examples/task-management-app-example.md](examples/task-management-app-example.md)

Contoh ini menunjukkan output dari setiap agent dan bagaimana integrate dengan superpowers skills.

---

## 🎯 Workflow Details

### Brainstorming → Rapid PRD

**Input ke Rapid PRD:**
```markdown
## Technical Considerations
- Preferred Stack: React + Node.js + PostgreSQL
- Infrastructure: Free tier only (Vercel + Railway)
- Performance: < 2s page load
- Experience Level: Comfortable with React, basic backend
```

**Output dari Rapid PRD:**
```markdown
## Tech Stack Decision

**Frontend:** React 18 + TypeScript + Vite
- ✅ Developer already comfortable with React
- ✅ TypeScript reduces bugs
- ⚠️ Bundle size (mitigate with code splitting)

**Backend:** Node.js + Express
- ✅ JavaScript full-stack (no context switching)
- ✅ Fast development
- ⚠️ Single-threaded (acceptable for small app)

## Data Model
User (id, email, passwordHash) → Profile (id, userId, name, avatar)
```

---

### Rapid PRD → Technical Breakdown

**Input ke Technical Breakdown:** Requirements + Tech Stack

**Output dari Technical Breakdown:**
```markdown
## Code Foundation

### Project Structure
my-app/
├── frontend/src/
│   ├── components/auth/  (LoginForm.tsx, RegisterForm.tsx)
│   ├── services/         (api.ts, auth.service.ts)
│   └── types/            (user.ts, task.ts)
└── backend/src/
    ├── routes/           (auth.routes.ts, task.routes.ts)
    ├── controllers/
    └── services/

### Code Conventions
- Components: PascalCase (UserProfile.tsx)
- Functions: camelCase (getUserData)
- Constants: UPPER_SNAKE_CASE (API_BASE_URL)

---

## Development Tasks

### Epic 1: Authentication (8 tasks)

#### Task 1.1: Create User Model
**Checklist:**
- [ ] Add User to prisma/schema.prisma
- [ ] Create migration
- [ ] Generate Prisma Client

**Files:**
- prisma/schema.prisma
- prisma/migrations/001_create_users.sql
- backend/src/types/user.ts

**Acceptance Criteria:**
- Migration runs successfully
- TypeScript types available
```

---

### Technical Breakdown → Implementation

**Copy tasks ke TodoWrite:**
```typescript
TodoWrite({
  todos: [
    {
      content: "Task 1.1: Create User Model",
      activeForm: "Creating user database model",
      status: "in_progress"
    }
  ]
})
```

**Lalu gunakan superpowers:**
```bash
/tdd  # Untuk auth logic (critical, butuh tests first)
/frontend-design  # Untuk UI components
/verification  # Sebelum mark complete
```

---

## 🛠️ Setup di Platform AI

### ChatGPT (Custom GPT)
1. Buat Custom GPT baru
2. Salin konten `prompts/01-brainstorming-agent.md` ke instructions
3. Set nama: "Brainstorming Agent"
4. Ulangi untuk agent 2 dan 3

### Claude (Projects)
1. Buat Project baru
2. Tambahkan `prompts/01-brainstorming-agent.md` ke project knowledge
3. Set custom instructions dari file tersebut
4. Ulangi untuk agent 2 dan 3

### Google Gemini (Gems)
1. Buat Gem baru
2. Salin konten prompt ke instructions
3. Ulangi untuk agent 2 dan 3

### Perplexity AI
1. Buka Settings → AI
2. Paste prompt ke custom instructions
3. Save

📖 **Panduan lengkap:** Lihat `SETUP-*.md` untuk step-by-step dengan screenshots.

---

## ✨ Key Features

### 1. 🌍 **Language-Agnostic & Platform-Universal**
- ✅ **Supports ANY programming language** (Python, Go, Swift, Rust, Java, Kotlin, JavaScript, C#, dll.)
- ✅ **Supports ANY platform** (Web, Mobile iOS/Android, CLI, Desktop, API, Game, Embedded)
- ✅ **Dynamic adaptation** - tidak hardcode JavaScript/React!
- ✅ Tanya tech stack preference di awal, lalu adapt semua output

### 2. Self-Contained Prompts
- ✅ Tidak perlu attach supporting files
- ✅ Semua context embedded di prompt
- ✅ Copy-paste langsung, ready to use
- ✅ **Lean prompts** (56% lebih kecil dari versi sebelumnya)

### 3. Actionable Output (Adaptive per Language)
- ✅ Technical tasks dengan **syntax yang benar** untuk bahasa pilihan
- ✅ File paths **sesuai convention** (snake_case untuk Python, camelCase untuk JS, dll.)
- ✅ Checklists yang jelas
- ✅ Testable acceptance criteria

### 4. Code Standards Included (Per Ecosystem)
- ✅ Project structure **per platform** (Django/Gin/SwiftUI/Spring Boot structure)
- ✅ Naming conventions **per language** (PEP 8/Go style/Apple guidelines/etc.)
- ✅ Testing strategy **per ecosystem** (pytest/go test/XCTest/JUnit/Jest/etc.)
- ✅ Git workflow specified

### 5. Superpowers Integration (Optional)
- ✅ TodoWrite compatible format
- ✅ Skill recommendations per epic
- ✅ Direct handoff workflow `/tdd`, `/verification`, `/code-review`

### 6. Flexible Language
- ✅ Output bisa English/Indonesian/Other
- ✅ Tanya di awal sesi

---

## 🎓 Best Practices

### 1. **Brainstorming Phase**
- Be honest tentang skill level (AI bisa suggest tech yang sesuai)
- Capture constraints upfront (budget, hosting, time)
- Don't skip technical exploration

### 2. **Rapid PRD Phase**
- Review tech stack reasoning (understand trade-offs)
- Prioritize ruthlessly (MVP first, no feature creep)
- Validate NFRs match your actual needs

### 3. **Technical Breakdown Phase**
- Review code foundation before task breakdown
- Understand dependencies (don't start Task 2 if it depends on Task 1)
- Use superpowers skills as recommended

### 4. **Implementation Phase**
- Follow code conventions defined in breakdown
- Use `/tdd` for critical business logic
- Use `/verification` before marking tasks complete
- Use `/code-review` before merging

---

## 🆚 vs Traditional Product Management Workflow

| Aspek | Traditional (5 Agents) | This Workflow (3 Agents) |
|-------|------------------------|--------------------------|
| **Agents** | Brainstorming → Brief → PRD → Architecture → Epics/Stories | Brainstorming → Rapid PRD → Technical Breakdown |
| **Time** | ~3-4 hours | ~1-2 hours (40% faster) |
| **Output** | Acceptance criteria (WHAT) | Technical tasks with file paths (HOW to code) |
| **Code Standards** | ❌ Not included | ✅ Included (conventions, testing, Git) |
| **Target** | Product team (PM + Dev) | Solo developer or small team |
| **Documentation** | Lengthy, stakeholder-friendly | Lean, actionable |
| **Implementation** | Manual breakdown needed | Direct to coding |

---

## 🤔 FAQ

### Q: Apakah bisa untuk team?
A: Bisa, tapi **tidak optimal**. Workflow ini designed untuk solo dev atau small team (2-3 orang). Untuk team besar dengan PM/PO terpisah, traditional workflow lebih cocok.

### Q: Apakah bisa skip Brainstorming?
A: Bisa, tapi **tidak recommended**. Brainstorming membantu eksplorasi alternatif teknikal yang mungkin lebih baik dari asumsi awal.

### Q: Apakah agent bisa auto-generate code?
A: **Tidak**. Output tetap task checklist, bukan actual code. Implementation manual dengan bantuan superpowers skills (`/tdd`, `/frontend-design`, dll).

### Q: Berapa lama dari ide sampai ready coding?
A: **1-2 jam** (tergantung kompleksitas project). Brainstorming ~30 min, Rapid PRD ~20 min, Technical Breakdown ~30-60 min.

### Q: Apakah bisa pakai di platform lain (non-Claude)?
A: **Yes!** Workflow ini platform-agnostic. Bisa dipakai di ChatGPT, Gemini, Perplexity, atau AI platform apapun yang support custom instructions.

### Q: Apakah output compatible dengan tools lain?
A: **Yes!** Output format markdown standar. Tasks compatible dengan:
- Superpowers TodoWrite (Claude Code)
- Jira/Linear/Asana (copy-paste tasks)
- GitHub Issues/Projects
- Notion/Obsidian

---

## 📖 Learn More

- **Design Rationale:** [docs/design-rationale.md](docs/design-rationale.md)
  - Kenapa workflow ini dibuat
  - Comparison detail dengan traditional workflow
  - Architecture decisions & trade-offs

---

## 🤝 Contributing

Kontribusi sangat diterima! Silakan:

- **Improve prompts** - Tingkatkan efektivitas agent prompts
- **Add examples** - Kontribusi contoh project lain
- **Fix issues** - Perbaiki bug atau typo
- **Share experience** - Bagikan pengalaman menggunakan workflow ini

**How to contribute:**
1. Fork repo ini
2. Buat branch baru (`git checkout -b feature/improvement`)
3. Commit changes (`git commit -m 'Add improvement'`)
4. Push ke branch (`git push origin feature/improvement`)
5. Buat Pull Request

---

## 📄 License

MIT License - Bebas digunakan, dimodifikasi, dan dibagikan.

---

## 🙏 Acknowledgments

- Workflow terinspirasi dari penggunaan Claude Code + superpowers skills
- Terima kasih untuk komunitas yang memberikan feedback
- Special thanks untuk solo developers yang test workflow ini

---

## 🚀 Ready to Start?

1. **Baca contoh:** [examples/task-management-app-example.md](examples/task-management-app-example.md)
2. **Setup agent:** Ikuti panduan di `SETUP-*.md`
3. **Start brainstorming:** Copy `prompts/01-brainstorming-agent.md` dan mulai!

**Happy Building!** 🎉

Transform ide Anda jadi code yang actionable, bukan sekedar dokumentasi yang numpuk.
