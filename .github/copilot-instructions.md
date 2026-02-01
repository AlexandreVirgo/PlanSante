# Copilot Instructions for PlanSanté

## Project Overview

**PlanSanté** is a structured personal health management system that combines data-driven tracking with cognitive role-based workflows. It's not a code repository—it's a decision-making framework for progressive health optimization (weight, fitness, sleep, nutrition).

This project uses **AIProjectFramework**: a structured approach to project governance combining:
- A **project registry** (definitive source of truth for project intent, scope, and state)
- **Role-based workflows** (executable procedures with explicit cognitive roles)
- **Iterative, human-gated decision-making** (agent suggests, human decides)

### Where to Find Information

For details on project goals, constraints, and current state:
→ **[project_registry.md](../project_registry.md)** (Authoritative reference — generated after first CORAL-P execution)

For executable workflows (procedures and their exact steps):
→ **`workflows/` folder** (Each workflow has its own `.md` file)

For cognitive role specifications:
→ **`roles/` folder** (Role-specific boundaries and capabilities)

---

## The Framework: Workflows and Roles

### What is a Workflow?

A **workflow** is a structured, multi-step procedure designed to solve a specific project problem. Each workflow:
- Has a **primary role** that guides decision-making (e.g., META-GOV-01)
- Is **human-gated**: Agent proposes, human validates before advancing
- Produces **concrete artifacts** (files, registries, logs)
- Is **fully documented** in its own `.md` file with exact inputs/outputs

### What is a Role?

A **role** is a cognitive posture—a set of explicit capabilities and boundaries that the agent adopts. Roles are:
- **Not autonomous decision-makers**: They structure, analyze, suggest
- **Explicitly bounded**: Each role has a detailed spec file defining what it can and cannot do
- **Non-overlapping**: Responsibilities are clear; no ambiguity about who does what

---

## Available Workflows in This Project

### Workflow Registry and Invocation

When you request to execute or resume a workflow, the agent will match your request against the registry.

**Authoritative source**: [workflows/WORKFLOW_REGISTRY.md](../workflows/WORKFLOW_REGISTRY.md)

---

## How to Invoke a Workflow

### Pattern 1: Start a workflow from the beginning
```
User: "Execute CORAL-P"
User: "Launch iris-r to define project roles"
User: "Run coral-p and help me build the project registry"

Agent action:
1. Identify workflow from keywords (consult WORKFLOW_REGISTRY.md)
2. Load the workflow file
3. Begin at § 4, Étape 1
4. Adopt the primary role listed in registry
5. Execute the first step
```

### Pattern 2: Resume from a specific step
```
User: "Resume CORAL-P at step 5"
User: "Reprendre coral-p à l'étape 4"
User: "Continue IRIS-R from étape 2"

Agent action:
1. Identify workflow and target step from request
2. Load the workflow file (reference WORKFLOW_REGISTRY.md)
3. Jump to § 4, Étape N (where N = requested step)
4. Adopt the primary role
5. Execute that step
```

### Pattern 3: Workflow with additional context (optional argument)
```
User: "Run IRIS-R and tell me if adding a Scribe role is appropriate"
User: "Execute CORAL-P for the new phase 2 project"

Agent action:
1. Identify workflow
2. Load the workflow file and begin normally
3. After completing the workflow, explicitly address the user's additional question/context
```

### Case Insensitivity
The agent recognizes workflow keywords regardless of case:
- `coral-p`, `CORAL-P`, `Coral-P`, `CoRaL-p` → all match
- `iris-r`, `IRIS-R`, `Iris-R`, `IRIS-r` → all match
- Verb variants accepted: run, execute, launch, start, begin, resume, continue, reprise, reprendre

---

## Self-Check Protocol

Before executing any workflow, the agent confirms:

✓ **Workflow identified**: [CORAL-P | IRIS-R | other]  
✓ **Entry point**: [Étape 1 | Étape N, where N = specific step]  
✓ **Authoritative source loaded**: [file path from registry]  
✓ **Primary role to assume**: [META-GOV-01 | other]  

**If uncertain**, display this to the user:
```
I'm about to execute [WORKFLOW]. Is this correct?
- Workflow: [NAME]
- File: [PATH]
- Entry point: [Étape X]
- Role: [ROLE]
```

Then await confirmation before proceeding.

---

## Critical Project Conventions

### Data Structure & Phases

- **Phase 1–N**: Structured progression periods within the health plan
- **Weekly tracking**: `data/phase{N}/S{WW}/` (e.g., `S24/` = week 24)
- **Two core artifacts per week**:
  - `bilan_semaine_XX.md`: Post-execution assessment (past-looking)
  - `plan_semaine_XX.md`: Action plan for the week (future-looking)
  - `R_HEBDO_S{WW}.md`: Weekly reference artifact summarizing decisions, indicators, and plans
- **Analysis files**: `data/phase{N}/S{WW}/analysis/a{X}.md`: intermediate analytical outputs

### Markdown Conventions & Project Patterns

This section documents observable patterns from the codebase. For formal definitions, consult the corresponding specification files.

#### Markdown Conventions

- **Headings hierarchy**: H1 (title), H2 (major sections), H3 (subsections)
- **Metadata blocks**: Sections like "## Objectifs de la semaine" or "## Alimentation" appear consistently in weekly plans
- **Status notation**:
  - `RAS` = Rien À Signaler (no changes)
  - `→` = continuation or implication arrow
- **Activity naming**: Standard codes like `FB-30-BASE-V1` (Functional Base, 30 min, base level, version 1)
- **RPE scale**: 1–10 Borg Rating of Perceived Exertion; context-specific (e.g., 5–6 for moderate running)

#### File Naming

- Phase files: `phase{N}.md` (N = 1, 2, 3, 4)
- Weekly files: `plan_semaine_{WW}.md` and `bilan_semaine_{WW}.md` (WW = week number)
- Analysis files: Sequential `a1.md`, `a2.md`, etc. under week's `analysis/` subdirectory
- Reference artifact: `R_HEBDO_Sxx.md` (weekly reference, created in Step 9)
- Templates: `template_*.md` in `workflows/cih/templates/`

---

## Critical Principles

- **Single source of truth**: All project state in [project_registry.md](../project_registry.md)
- **Governance by design**: Every major decision is human-gated (agent proposes, human decides)
- **Role respect**: Each workflow has explicit role boundaries; don't exceed them
- **Artifact traceability**: Workflows produce logs; check `workflows/[name]/logs/` for execution history
- **No autonomous decisions**: If uncertain, ask the user

---

## When Uncertain, Consult

- **Workflow registry**: [workflows/WORKFLOW_REGISTRY.md](../workflows/WORKFLOW_REGISTRY.md)
- **Workflow protocol**: The relevant workflow `.md` file
- **Role boundaries**: The corresponding `roles/[role-name].md` file
- **Project state**: [project_registry.md](../project_registry.md) (available after CORAL-P initialization)
- **This document**: For workflow invocation syntax and keywords
