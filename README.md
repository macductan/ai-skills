# AI Skills 🚀

A comprehensive repository of custom AI skills, prompts, workflows, and system rules designed for AI coding agents (such as Claude). These skills help agents operate with specific developer personas, follow strict coding guidelines, and implement structured workflows.

## 🎯 Features

- **Standardized Workflows**: Predefined step-by-step processes to ensure AI agents tackle problems methodically rather than rushing to code.
- **Strict Developer Personas**: Tailored system prompts enforcing senior-level practices, such as explicitly surfacing assumptions, managing confusion, and valuing code simplicity.
- **Agent Orchestration**: Guidelines for planning, verification, and using subagents efficiently to manage complex projects.

## 📁 Repository Structure

```text
ai-skills/
├── skills/
│   ├── code-reviewer-skill/
│   │   └── SKILL.md      # Skill defining the Senior Code Reviewer persona
│   ├── init-memory-bank/
│   │   └── SKILL.md      # Skill to initialize a Memory Bank for any project
│   └── solution-architect/
│       └── SKILL.md      # Skill defining the Solution Architect & Senior SWE persona
├── README.md
```

## ✨ Available Skills

### 1. Solution Architect + Senior Software Engineer

**Path:** `skills/solution-architect/SKILL.md`

This skill instructs the AI to adopt the persona of an uncompromising, senior-level software engineer working side-by-side with a human developer. It heavily focuses on:

- **Assumption Surfacing**: Always stating assumptions explicitly before acting.
- **Confusion Management**: Never guessing when facing ambiguous requirements.
- **Simplicity Enforcement**: Preventing over-engineering and bloated abstractions.
- **Scope Discipline**: Touching only what needs to be touched; avoiding untracked cleanups.

#### 🔄 The 5-Step Workflow

This skill enforces a robust 5-step development loop, managed via short commands:

1. **`start`**: Loads project context (Memory Bank) in read-only mode.
2. **`init`**: Analyzes the problem and generates clarify questions and architecture proposals in `ai/architect/phase1-analysis.md`.
3. **`plan`**: Creates a step-by-step implementation plan in `ai/architect/phase2-implementation.md`.
4. **`discuss`**: A sync point. Parses human feedback and inline discussions, adjusting the task scope or converting items into bugs.
5. **`run`**: Executes the approved implementation, tracking progress state.

### 2. Init Memory Bank

**Path:** `skills/init-memory-bank/SKILL.md`

This skill instructs the AI to act as a System Architect that scans your entire project, analyzes configuration files and source code, and automatically generates a structured **Memory Bank** — a set of markdown files that capture the project's context, tech stack, architecture patterns, and current state.

#### Generated Files

- `memory-bank/projectbrief.md` — Project summary and core objectives.
- `memory-bank/techContext.md` — Tech stack, key libraries, and environment setup.
- `memory-bank/systemPatterns.md` — Architecture patterns and coding principles.
- `memory-bank/activeContext.md` — Current codebase state and in-progress work.

The skill presents an Implementation Plan for approval before writing any files.

### 3. Code Reviewer + Senior Software Engineer

**Path:** `skills/code-reviewer-skill/SKILL.md`

This skill instructs the AI to adopt the persona of a Senior Code Reviewer with 20+ years of experience. It focuses on scrutinizing code, catching bugs, optimizing performance, and protecting codebase quality against 6 pillars: Efficiency, Readability, Maintainability, Security, Bugs & Edge Cases, and Best Practices.

#### 🔄 The 4-Step Code Review Workflow

This skill enforces a step-by-step code review and fix loop:

1. **`diff`**: Gathers git changes compared to the main branch and saves them to a raw diff file.
2. **`audit`**: Analyzes the diff based on the 6 evaluation pillars and generates a detailed review report.
3. **`discuss`**: Reads user feedback on the report, responding inline or updating the status of issues (e.g., to "Needs Auto-Fix" or "Ignored").
4. **`fix`**: Automatically goes into the source code and applies finalized fixes for approved issues.

## 🛠 Usage

You can install these skills directly into your project using the `npx skills` command:

```bash
# Install the Solution Architect skill
npx skills add https://github.com/macductan/ai-skills --skill solution-architect

# Install the Init Memory Bank skill
npx skills add https://github.com/macductan/ai-skills --skill init-memory-bank

# Install the Code Reviewer skill
npx skills add https://github.com/macductan/ai-skills --skill code-reviewer-skill
```

Alternatively, you can manually clone and integrate them:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/macductan/ai-skills.git
   ```
2. **Integrate into your AI Agent Workspace**:
   Depending on your specific AI tool, install or copy the `skills` folder into your working project or agent's system directory (e.g., `.agents/skills/` or similar configuration folders).
3. Ensure your agent reads the instructions located within the `SKILL.md` files upon initialization.

## 🤝 Contributing

Contributions are welcome! If you have curated optimized prompts, custom agent workflows, or other specialized personas:

1. Fork the repository.
2. Create a new skill directory under `skills/` (e.g., `skills/frontend-expert/`).
3. Add your detailed `SKILL.md` instructions.
4. Submit a Pull Request.

---

_Built to empower Human-AI pair programming._
