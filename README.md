# Dynamind — Universal Memory Bank Engine

Dynamind enables structured knowledge hubs for any complex domain: systems, hobbies, endeavors, businesses, research areas, or long-running efforts.

This repository contains the scaffolding rules and templates that power any "dynamind"—providing robust patterns, workflows, and structure for persistent knowledge management through Cline.

---

## Prerequisites

### What You Need

**Cline AI Assistant**
- Dynamind works through [Cline](https://cline.bot), an AI coding assistant that runs in VSCode
- Cline enables natural language interaction with your knowledge base
- Memory resets between sessions, making Dynamind's persistent documentation critical

**Installation:**
1. Install [Visual Studio Code](https://code.visualstudio.com/)
2. Install the [Cline extension](https://marketplace.visualstudio.com/items?itemName=saoudrizwan.claude-dev)
3. Configure your API key (Claude, OpenAI, etc.)
   - See [Cline's Getting Started Guide](https://docs.cline.bot/getting-started)
   - Need help choosing a model? Check [Model Selection Guide](https://docs.cline.bot/model-selection)

**First time with Cline?**
- Read: [Cline Documentation](https://docs.cline.bot)
- Watch: [Cline Quick Start Video](https://docs.cline.bot/getting-started)

---

## What is a Dynamind?

A dynamind is a memory-bank-powered knowledge hub that:
- **Persists context** across Cline sessions (critical since memory resets)
- **Organizes** complex information into structured patterns
- **Enables** planning and executing projects within its scope
- **Maintains** relationships between different focus areas
- **Adapts** organically as knowledge evolves

Within a dynamind, you can manage multiple **focus areas** (research, platforms, learning, etc.) with specific **focuses** (topics, projects, initiatives) while maintaining shared patterns and knowledge.

**Think of it as:** A living knowledge base that remembers everything for you, organized exactly how you need it.

---

## Quick Start

### 1. Clone or Download This Repository

```bash
# Clone to your local machine
git clone https://github.com/neilsone/dynamind.git
cd dynamind

# Or download and extract the ZIP file
```

### 2. Open in VSCode with Cline

```bash
# Open this directory in VSCode
code .
```

Make sure the Cline extension is installed and activated (look for the Cline icon in the sidebar).

### 3. Initialize Your Memory Bank

In Cline's chat interface, simply say:

```
Initialize the dynamind memory bank for [your domain]
```

**Examples:**
- "Initialize the dynamind memory bank for my web development projects"
- "Initialize the dynamind memory bank for my machine learning research"
- "Initialize the dynamind memory bank for learning Spanish"

**What Happens:**
Cline will create:
- `memory-bank/` directory with 6 core documentation files
- `memory-bank/focus-index.md` to track all your focuses
- Initial structure customized to your domain

### 4. Create Your First Focus

```
Create a focus called [topic] in the [area] focus area
```

**Examples:**
- "Create a focus called react-components in the frontend focus area"
- "Create a focus called transformer-models in the research focus area"
- "Create a focus called grammar in the learning focus area"

**What Happens:**
Cline will:
- Validate naming conventions (lowercase, hyphens, underscores only)
- Create `focus-areas/[area]/focus-sections/[topic]/OVERVIEW.md`
- Add TODOs for you to fill in specific details
- Update the focus index
- Optionally create additional context files

### 5. Start Working!

Now you can:
- Ask Cline to open any focus: `"Open the react-components focus"`
- Update context: `"Update context for react-components"`
- List everything: `"List all focuses"`
- Navigate naturally: Cline reads your memory bank automatically

---

## Example Workflows

### Software Engineer Managing a Side Project

```
1. "Initialize the dynamind memory bank for my task manager app"
2. "Create a focus called backend-api in the development focus area"
3. "Create a focus called frontend-ui in the development focus area"
4. "Open the backend-api focus"
   [Work on backend, then...]
5. "Update memory bank" 
   [Cline updates all context with your progress]
6. "Switch to the frontend-ui focus"
   [Continue with full context maintained]
```

### Researcher Organizing Literature

```
1. "Initialize the dynamind memory bank for my PhD research on climate models"
2. "Create a focus called data-analysis in the methodology focus area"
3. "Create a focus called literature-review in the research focus area"
4. "What's the status of literature-review?"
   [Check current state]
5. "Update context for literature-review with recent papers"
6. "Create dependency matrix for methodology"
   [Track relationships between methods]
```

### Learning a New Skill

```
1. "Initialize the dynamind memory bank for learning piano"
2. "Create a focus called music-theory in the fundamentals focus area"
3. "Create a focus called practice-pieces in the repertoire focus area"
4. "List all focuses"
   [See your learning structure]
5. "Update memory bank"
   [Capture progress and insights]
```

---

## Understanding Cline's Modes

Cline operates in two modes:

### 🎯 Plan Mode (Default)
- **Purpose:** Gather information, ask questions, create detailed plans
- **Use when:** Starting new work, exploring options, making decisions
- **Dinamind behavior:** Reads memory bank, discusses approach, gets your approval
- **Example:** "Should I use REST or GraphQL for this API?"

### ⚡ Act Mode
- **Purpose:** Execute tasks and make changes
- **Use when:** Ready to implement a plan
- **Dynamind behavior:** Creates files, updates documentation, executes work
- **Example:** Actually creates the API files and updates memory bank

**Toggle between modes** using the Plan/Act button in Cline's interface.

---

## Directory Structure

```
.clinerules/                    # Scaffolding rules & templates
  dynamind.md                   # Core rules (defines all behavior)
  templates/                    # Templates for creating focuses
    focus/                      # Focus-level templates
      OVERVIEW.md.template
      CLINE.md.template
      architecture.md.template
      status.md.template
      [more templates...]
    focus-area/                 # Focus-area templates
    dynamind/                   # Dynamind-level templates
    linkage-matrix.md.template

memory-bank/                    # Core documentation (created by Cline)
  dynamindBrief.md             # Requirements, goals, scope
  dynamindContext.md           # Rationale, vision
  dynamindActiveContext.md     # Current state, decisions
  dynamindPatterns.md          # Reusable patterns
  techContext.md              # Technologies, constraints
  dynamindProgress.md         # Status log
  focus-index.md              # Registry of all focuses

focus-areas/                   # Your domain-specific organization
  [focus-area]/                # e.g., "research", "development"
    focus-sections/
      [focus-section]/         # Specific focus topic
        OVERVIEW.md           # Required: summary, owner, links
        CLINE.md             # Optional: navigation guide
        *.md                 # Optional: architecture, status, etc.
```

---

## Core Memory Bank Files

Every dynamind has 6 core files that Cline reads at the start of every task:

1. **dynamindBrief.md** — Foundation: requirements, goals, scope
2. **dynamindContext.md** — Rationale and vision  
3. **dynamindPatterns.md** — Reusable architecture patterns
4. **techContext.md** — Technologies and constraints
5. **dynamindActiveContext.md** — Current state and decisions
6. **dynamindProgress.md** — Status log and issues

**Reading Order:** Brief → Context → Patterns → Tech → Active → Progress

This order ensures Cline always has complete context before making suggestions or changes.

---

## Working with Focuses

### Natural Language Commands

| Say This | Cline Does This |
|----------|----------------|
| "Create focus X in area Y" | Validates names, scaffolds OVERVIEW.md, updates index |
| "List all focuses" | Shows focuses grouped by area with links |
| "Open focus X" | Navigates, reads CLINE.md then OVERVIEW.md |
| "Update context for X" | Updates focus files and matrices |
| "Create dependency matrix for Y" | Scaffolds relationship matrix |
| "What's the status of X?" | Reads status, checks progress |
| "Switch to focus Y" | Finalizes current work, opens new focus |

### Focus Naming Rules

✅ **Valid:**
- `backend-api`
- `literature_review`
- `chapter-01`
- `ml-models-2024`

❌ **Invalid:**
- `Backend API` (no spaces)
- `backend/api` (no slashes)
- `backend.api` (no periods)
- `Backend-API` (no capitals)

**Rules:** Lowercase letters, numbers, hyphens, underscores only. No spaces or special characters.

---

## Memory Bank Updates

### When to Update

1. **After significant work** — Capture what you accomplished
2. **Say the trigger phrase** — "update memory bank" or "update dynamind"
3. **When patterns emerge** — Document reusable solutions
4. **When context changes** — Keep documentation current

### What Gets Updated

When you request a memory bank update, Cline performs a **comprehensive review** of:

- ✅ ALL 6 core memory-bank files (not just what changed)
- ✅ Focus-specific files with new information
- ✅ Extracted patterns added to `dynamindPatterns.md`
- ✅ Cross-linkage matrices if relationships evolved
- ✅ **Always:** `dynamindActiveContext.md` and `dynamindProgress.md`

**Critical:** "Update memory bank" means reviewing everything, not just recently changed files.

---

## Tips & Best Practices

### 🎯 Effective Memory Bank Usage

**Do:**
- ✅ Update memory bank after completing significant work
- ✅ Extract patterns when you solve problems that could recur
- ✅ Keep focus OVERVIEW.md files concise and actionable
- ✅ Use natural language—Cline understands intent
- ✅ Let documentation evolve organically

**Don't:**
- ❌ Over-organize initially—start simple and expand as needed
- ❌ Duplicate information across files—link instead
- ❌ Wait too long between updates—context gets stale
- ❌ Force rigid structures—adapt templates to your needs

### 📁 Focus Management

**Create new focuses when:**
- Topics are distinct and can be worked on independently
- You need separate documentation and decision tracking
- Different concerns or domains emerge

**Expand existing focuses when:**
- Topics are closely related and share context
- Changes affect the same area
- It's a continuation of existing work

**Example:**
- ✅ Good: `backend-api` and `database-schema` as separate focuses (different concerns)
- ❌ Overkill: `user-authentication` and `user-authorization` as separate (too granular, combine into `backend-auth`)

### 🔗 Linking and Navigation

- Use CLINE.md files in focuses for complex navigation
- Link to external resources liberally (repos, docs, diagrams)
- Create linkage matrices when you have 50+ focuses or complex dependencies
- Keep patterns in `dynamindPatterns.md` to avoid duplication

---

## Large-Scale Systems

For dynaminds with 50+ focuses, create relationship matrices:

**When to use:**
- Dependencies and data flows exceed what hierarchy can show
- You need to track cross-cutting concerns
- Regional or logical groupings become important

**Where to create:**
- Focus-area level for area-specific relationships
- Memory-bank level for system-wide views

**How:**
- Use `.clinerules/templates/linkage-matrix.md.template`
- Customize with your specific relationship types
- Keep updated as system evolves

**Examples:**
- "Focus Dependency Matrix" — Which focuses depend on each other
- "Data Flow Table" — How information moves between focuses
- "Regional Grouping" — Geographic or logical organization

---

## Cline Resources

### Official Documentation
- **Getting Started:** https://docs.cline.bot/getting-started
- **Model Selection:** https://docs.cline.bot/model-selection
- **Features Guide:** https://docs.cline.bot/features
- **Prompt Engineering:** https://docs.cline.bot/prompt-engineering

### Useful Guides
- **Task Management:** https://docs.cline.bot/task-management
- **MCP Servers:** https://docs.cline.bot/mcp (for advanced integrations)
- **Workflows:** https://docs.cline.bot/features/workflows

### Community & Support
- **GitHub:** https://github.com/cline/cline
- **Discord:** Join the Cline community for questions and discussions

---

## Frequently Asked Questions

### Q: What if the memory bank isn't created?

**A:** Ensure you're in Act Mode (toggle from Plan Mode) when asking Cline to initialize. If still having issues, try: "I need you in Act Mode to initialize the memory bank for [domain]"

### Q: How do I know if Cline is reading the rules?

**A:** Cline automatically reads `.clinerules/dynamind.md` on startup. You can verify by asking: "What rules are you following?" Cline should mention dynamind scaffolding.

### Q: Can I use Dynamind without Cline?

**A:** Technically yes—the memory bank structure works standalone. However, Cline's natural language interface and automatic rule-following make Dynamind 100x more effective. Without Cline, you'd manually maintain all files.

### Q: What happens if I make a mistake in focus naming?

**A:** You can rename manually (update directory and references) or ask Cline: "Rename the [old-name] focus to [new-name] and update all references."

### Q: How much does this cost?

**A:** Dynamind itself is free (MIT license). Costs depend on your Cline API usage (Claude, OpenAI, etc.). Typical usage: $0.10-$2 per day for active development.

### Q: Can I have multiple dynaminds?

**A:** Absolutely! Each domain/project can be its own dynamind. Just create separate directories. Some users have dozens of dynaminds for different aspects of their work.

---

## Philosophy

- **Universal scope** — Any complex domain works (systems, hobbies, endeavors, long-running efforts)
- **Natural conversation** — No command syntax required
- **Intelligent defaults** — Infer intent from context
- **Adaptive content** — Templates guide, reality determines
- **Organic evolution** — Patterns emerge from use
- **Cline-native** — Seamless integration
- **Memory-first** — After reset, documentation is everything

---

## Upgrading

To get the latest dynamind rules and templates:

1. **Backup your content:**
   ```bash
   # Your memory-bank/ and focus-areas/ are safe
   # But backup just in case
   cp -r memory-bank memory-bank.backup
   cp -r focus-areas focus-areas.backup
   ```

2. **Pull or download updates:**
   ```bash
   git pull origin main
   # Or re-download and replace .clinerules/ directory
   ```

3. **Verify:**
   - Latest `.clinerules/dynamind.md` and templates are updated
   - Your `memory-bank/` and `focus-areas/` remain unchanged
   - Ask Cline: "What version of dynamind rules are you using?"

---

## Contributing

Found a bug or have a suggestion? Contributions are welcome!

1. Fork this repository
2. Create a feature branch
3. Make your improvements
4. Submit a pull request

**Guidelines:**
- Keep rules concise and conflict-free
- Add templates that solve real needs
- Update documentation with examples
- Test with actual Cline usage

---

## License

MIT License - See [LICENSE](LICENSE) file for details.

Copyright (c) 2025 Neilson P. Eney

---

## Acknowledgments

Built for the [Cline](https://cline.bot) AI assistant community.

Special thanks to all contributors who help make knowledge management seamless and accessible.
