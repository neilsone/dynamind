# Dynamind — Universal Memory Bank Engine

Dynamind enables structured knowledge hubs for any complex domain: systems, hobbies, endeavors, businesses, research areas, or long-running efforts.

This repository contains the scaffolding rules and templates that power any "dynamind"—providing robust patterns, workflows, and structure for persistent knowledge management through Cline.

---

## What is a Dynamind?

A dynamind is a memory-bank-powered knowledge hub that:
- Persists context across Cline sessions (critical since memory resets)
- Organizes complex information into structured patterns
- Enables planning and executing projects within its scope
- Maintains relationships between different focus areas
- Adapts organically as knowledge evolves

Within a dynamind, you can manage multiple focus areas (research, platforms, learning, etc.) with specific focuses (topics, projects, initiatives) while maintaining shared patterns and knowledge.

---

## Quick Start

### 1. Use This Directory as Your Dynamind

This directory IS your dynamind. It contains:
- `.clinerules/dynamind.md` — The scaffolding rules
- `.clinerules/templates/` — Templates for creating focuses
- Core files to manage your knowledge hub

### 2. Initialize Your Memory Bank

With Cline, simply say:

```
Initialize the dynamind memory bank for [your domain/system/hobby]
```

Cline will create:
- `memory-bank/` with 6 core files
- `memory-bank/focus-index.md` to track all focuses
- Initial structure based on your domain

### 3. Create Your First Focus

```
Create a focus called [topic] in the [area] focus area
```

Cline will:
- Validate naming conventions
- Scaffold `OVERVIEW.md` with TODOs
- Update the focus index
- Create optional context files as needed

---

## Directory Structure

```
.clinerules/                    # Scaffolding rules & templates
  dynamind.md                   # Core rules (this defines behavior)
  templates/                    # Focus templates

memory-bank/                    # Core documentation (created by Cline)
  dynamindBrief.md             # Requirements, goals, scope
  dynamindContext.md           # Rationale, vision
  dynamindActiveContext.md     # Current state, decisions
  dynamindPatterns.md          # Reusable patterns
  techContext.md              # Technologies, constraints
  dynamindProgress.md         # Status log
  focus-index.md              # Registry of all focuses

focus-areas/                   # Domain-specific organization
  [focus-area]/                # e.g., "research", "learning"
    focus-sections/
      [focus-section]/         # Specific focus
        OVERVIEW.md           # Required
        CLINE.md             # Optional navigation
        *.md                 # Optional docs
```

---

## Core Memory Bank Files

Every dynamind has 6 core files that must be read at the start of every task:

1. **dynamindBrief.md** — Foundation: requirements, goals, scope
2. **dynamindContext.md** — Rationale and vision
3. **dynamindPatterns.md** — Reusable architecture patterns
4. **techContext.md** — Technologies and constraints
5. **dynamindActiveContext.md** — Current state and decisions
6. **dynamindProgress.md** — Status log and issues

**Reading Order:** Brief → Context → Patterns → Tech → Active → Progress

---

## Working with Focuses

### Natural Language Commands

| Say This | Cline Does This |
|----------|----------------|
| "Create focus X in area Y" | Validates names, scaffolds OVERVIEW.md, updates index |
| "List all focuses" | Shows grouped by area with links |
| "Open focus X" | Navigates, reads CLINE.md then OVERVIEW.md |
| "Update context for X" | Updates focus files and matrices |
| "Create dependency matrix for Y" | Scaffolds linkage matrix |
| "What's the status of X?" | Reads status, OVERVIEW, checks progress |

### Focus Naming Rules

- Lowercase letters, numbers, hyphens, underscores only
- No spaces or special characters
- Descriptive but concise

---

## Memory Bank Updates

### When to Update

1. After significant work or discoveries
2. Say "update memory bank" or "update dynamind"
3. When new patterns emerge
4. When context needs clarification

### What Gets Updated

- ALL 6 core memory-bank files (comprehensive review)
- Focus-specific files with new information
- Extracted patterns to `dynamindPatterns.md`
- Cross-linkage matrices if relationships changed
- Always: `dynamindActiveContext.md` and `dynamindProgress.md`

**Critical:** "Update memory bank" means reviewing everything, not just changed files.

---

## Large-Scale Systems

For dynaminds with 50+ focuses, create relationship matrices:
- **When:** Dependencies/flows exceed hierarchy
- **Where:** Focus-area or memory-bank level
- **How:** Use `linkage-matrix.md.template`
- **Examples:** Dependency Matrix, Data Flow Table, Regional Grouping

---

## Philosophy

- **Universal scope** — Any complex domain works
- **Natural conversation** — No command syntax
- **Intelligent defaults** — Infer intent
- **Adaptive content** — Templates guide, reality determines
- **Organic evolution** — Patterns emerge from use
- **Cline-native** — Seamless integration
- **Memory-first** — After reset, documentation is everything

---

## Upgrading

To get the latest dynamind rules:

1. Pull updates to this repository
2. Latest `.clinerules/dynamind.md` and templates will be available
3. Your `memory-bank/` and `focus-areas/` remain unchanged

---

## License

MIT License - See [LICENSE](LICENSE) file for details.

Copyright (c) 2025 Neilson P. Eney
