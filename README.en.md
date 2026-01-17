# Idea to Epic Workflow AI Prompts

A collection of AI prompts to transform ideas into development-ready Epics & Stories. Works with any AI platform (Perplexity, Google Gems, ChatGPT, Claude, etc.).

> 🌐 [Versi Bahasa Indonesia](README.md)

## Overview

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  Brainstorming  │────▶│  Product Brief  │────▶│      PRD        │
│     Agent       │     │     Agent       │     │     Agent       │
└─────────────────┘     └─────────────────┘     └─────────────────┘
                                                        │
                        ┌───────────────────────────────┘
                        ▼
┌─────────────────┐     ┌─────────────────┐
│  Architecture   │────▶│ Epics & Stories │────▶  Ready for
│     Agent       │     │     Agent       │      Development
└─────────────────┘     └─────────────────┘
```

## Quick Start

1. Pick an AI platform (Perplexity, Google Gems, ChatGPT, Claude)
2. Copy a prompt file content into the AI's custom instructions
3. (Optional) Attach the corresponding supporting file for better context
4. Follow the guided workflow

## Files

```
product-dev-workflow/
├── README.md                    # Bahasa Indonesia (default)
├── README.en.md                 # This file (English)
├── LICENSE                      # MIT License
├── prompts/
│   ├── 01-brainstorming-agent.md
│   ├── 02-product-brief-agent.md
│   ├── 03-prd-agent.md
│   ├── 04-architecture-agent.md
│   └── 05-epics-stories-agent.md
└── supporting/                  # Optional reference files
    ├── 01-brainstorming-techniques.md
    ├── 02-product-brief-questions.md
    ├── 03-prd-requirements-framework.md
    ├── 04-architecture-decision-framework.md
    └── 05-epics-stories-guide.md
```

## The 5 Agents

| #   | Agent               | Role                 | What It Does                               |
| --- | ------------------- | -------------------- | ------------------------------------------ |
| 1   | **Brainstorming**   | Creative Facilitator | Explores ideas, identifies opportunities   |
| 2   | **Product Brief**   | Business Analyst     | Defines problem, solution, success metrics |
| 3   | **PRD**             | Product Manager      | Documents requirements (FR/NFR)            |
| 4   | **Architecture**    | Software Architect   | Designs technical solution                 |
| 5   | **Epics & Stories** | Product Owner        | Creates implementation-ready stories       |

## How to Use

### Step 1: Brainstorming

```
1. Set up Brainstorming Agent in your AI platform
2. Provide your initial idea or problem
3. Follow the interactive session
4. Save the output
```

### Step 2: Product Brief

```
1. Set up Product Brief Agent
2. Paste your brainstorming output
3. Answer clarifying questions
4. Save the output
```

### Step 3: PRD

```
1. Set up PRD Agent
2. Paste your Product Brief
3. Review requirements and priorities
4. Save the output
```

### Step 4: Architecture

```
1. Set up Architecture Agent
2. Paste your PRD
3. Discuss tech constraints and decisions
4. Save the output
```

### Step 5: Epics & Stories

```
1. Set up Epics & Stories Agent
2. Paste both PRD and Architecture docs
3. Review epic structure and stories
4. Save the output → Ready for development!
```

## Platform Setup

### Google Gems

1. Gemini → Gems → Create Gem
2. Paste prompt content into Instructions
3. (Optional) Add supporting file
4. Save and use

### Perplexity

1. Start new conversation
2. Attach or paste prompt file
3. (Optional) Attach supporting file
4. Begin session

### ChatGPT

1. Explore GPTs → Create
2. Paste prompt into Instructions
3. (Optional) Upload supporting file to Knowledge
4. Publish and use

### Claude

1. Projects → New Project
2. Add prompt to Project Knowledge
3. (Optional) Add supporting file
4. Start conversation

## Features

- ✅ **Modular** - Use any agent standalone or in sequence
- ✅ **Platform-agnostic** - Works with any AI platform
- ✅ **Semi-guided** - Checkpoints for validation
- ✅ **Flexible language** - Choose your output language
- ✅ **Implementation-ready** - Output focuses on WHAT, not HOW

## Supporting Files

Each agent has a corresponding supporting file with additional context:

| Agent           | Supporting File                         | Contains                        |
| --------------- | --------------------------------------- | ------------------------------- |
| Brainstorming   | `01-brainstorming-techniques.md`        | SCAMPER, Six Hats, Mind Mapping |
| Product Brief   | `02-product-brief-questions.md`         | Discovery questions, metrics    |
| PRD             | `03-prd-requirements-framework.md`      | FR/NFR templates, user stories  |
| Architecture    | `04-architecture-decision-framework.md` | ADR templates, tech evaluation  |
| Epics & Stories | `05-epics-stories-guide.md`             | Story writing, WHAT vs HOW      |

Attaching these files improves output quality but is optional.

## License

MIT License - Feel free to use, modify, and share.

## Contributing

Contributions welcome! Feel free to:

- Improve prompt effectiveness
- Add new supporting materials
- Fix issues or typos
- Share your experience
