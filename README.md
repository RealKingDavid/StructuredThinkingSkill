# Structured Thinking Skill for AI Agents

A skill that transforms any idea — no matter how vague or complex — into a clear, phased plan with granular, executable tasks. Built for founders, designers, engineers, and creatives who want Claude (or any AI agent) to help structure their thinking and break down complex problems.

## What are Skills?

Skills are markdown files that give AI agents specialized knowledge and workflows for specific tasks. When you add this skill to your project, your AI agent can recognize when you're working through an idea and apply the right frameworks, frameworks, and best practices automatically.

## Available Skills

| Skill | Description |
| --- | --- |
| [structured-thinking](./skills/structured-thinking) | Break down any complex idea into phases, tasks, and subtasks — tailored to business, product, creative, or technical contexts |

## What It Does

Given any idea, the skill will:

1. **Ask a few focused questions** to understand scope, constraints, and goals
2. **Classify the idea type** — business/startup, product/UX design, creative project, or technical/engineering
3. **Generate a tailored framework** with 3–5 phases, tasks per phase, and granular subtasks
4. **Surface key risks and decisions** to watch out for
5. **Recommend your first 3 actions** to build immediate momentum

## Example Prompts

```
"I have an idea for a meal-prep delivery service"
→ Business/startup framework: validate → define → build → go-to-market → scale

"Help me design an onboarding flow for my app"
→ Product/UX framework: discover → ideate → prototype → test → handoff

"I want to write a sci-fi novel"
→ Creative framework: concept → structure → draft → revise → publish

"I need to build a REST API for my platform"
→ Technical framework: define → architect → build → test → deploy
```

## Installation

### Option 1: CLI Install (Recommended)

```bash
# Install globally (works across all projects)
npx skills add <your-username>/StructuredThinkingSkill -g -y

# Install to current project only
npx skills add <your-username>/StructuredThinkingSkill -y
```

### Option 2: Manual Install

```bash
# Clone the repo
git clone https://github.com/<your-username>/StructuredThinkingSkill.git

# Copy to your agent's skills folder
# For Claude Code:
mkdir -p ~/.claude/skills
cp -r StructuredThinkingSkill/skills/structured-thinking ~/.claude/skills/

# For Cursor:
mkdir -p ~/.cursor/skills
cp -r StructuredThinkingSkill/skills/structured-thinking ~/.cursor/skills/
```

### Option 3: Direct Download

Download the `skills/structured-thinking/` folder and drop it into your AI agent's skills directory.

### Uninstall

```bash
npx skills remove structured-thinking

# Or manually:
rm -rf ~/.claude/skills/structured-thinking
rm -rf ~/.cursor/skills/structured-thinking
```

## Supported AI Agents

This skill works with any agent that supports markdown skill files:

- **Claude Code** (CLI)
- **Cursor** (IDE)
- **Windsurf**
- **Codex**
- **Gemini CLI**
- **OpenCode**
- And 30+ more

## Skill Structure

```
structured-thinking/
├── SKILL.md                    # Core skill — trigger logic, process, output format
└── references/
    ├── business-startup.md     # Phases & tasks for startup/business ideas
    ├── product-ux.md           # Phases & tasks for product/UX design
    ├── creative.md             # Phases & tasks for creative projects
    └── technical.md            # Phases & tasks for engineering/technical builds
```

The skill reads only the reference file that matches your idea type — keeping responses focused and relevant.

## Usage

Once installed, just describe your idea to your AI assistant:

```
"I want to launch a B2B SaaS tool for small law firms"
→ structured-thinking activates with a business/startup framework

"Help me think through building a design system from scratch"
→ structured-thinking activates with a product/UX framework

"I want to create a YouTube channel about personal finance"
→ structured-thinking activates with a creative framework

"I need to architect a real-time notification system"
→ structured-thinking activates with a technical framework
```

## Why This Skill Matters

**The Problem:**
- Most ideas stall at the "I have an idea" stage
- People don't know where to start or what order to do things in
- Generic advice doesn't account for the type of problem you're solving
- Complexity feels overwhelming without a structure to hold it

**The Solution:**
- A clear, phased framework tailored to your specific idea type
- Granular subtasks that are actually executable, not vague
- Honest timelines and risk flags — no sugarcoating
- Immediate next steps so you can start today

## Contributing

Have an idea to improve this skill? Found a gap in one of the frameworks? PRs and issues are welcome!

See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

## License

MIT License — use it however you want.

See [LICENSE](./LICENSE) for details.

---

*Built to help anyone with a great idea figure out what to do next.*
