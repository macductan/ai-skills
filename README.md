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

## 🛠 Usage

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/ai-skills.git
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
