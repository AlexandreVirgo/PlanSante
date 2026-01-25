# Copilot Instructions for PlanSanté

## Project Overview

**PlanSanté** is a structured personal health management system that combines data-driven tracking with cognitive role-based workflows. It's not a code repository—it's a decision-making framework for progressive health optimization (weight, fitness, sleep, nutrition).

### Core Framework: Cadre d'Itération Hebdomadaire (CIH)

The project uses a **weekly iteration protocol** with 9 sequential cognitive roles:
1. **PS-ANA-02** (Analyst): Comparative trend analysis of health data
2. **PS-SIG-05** (Signal Detection): Identify subtle patterns and anomalies
3. **PS-COH-04** (Coherence Check): Validate internal consistency (pre-decision)
4. **PS-STR-01** (Structuring): Organize findings into clear statements
5. **PS-DIR-07** (Strategic Direction): Frame options within project constraints
6. **Human Decision Point** (non-delegable)
7. **PS-PLAN-08** (Planning): Convert decisions into concrete weekly actions
8. **PS-COH-04** (Coherence Check): Post-decision validation (optional)
9. **PS-SCR-06** (Recording): Archive decisions and update reference artifacts

Each role has **explicit inputs, outputs, and cognitive boundaries**. Roles do not validate each other's work or make decisions.

## Critical Project Conventions

### Data Structure & Phases

- **Phase 1–N**: Structured progression periods within the health plan
- **Weekly tracking**: `data/phase{N}/S{WW}/` (e.g., `S24/` = week 24)
- **Two core artifacts per week**:
  - `bilan_semaine_XX.md`: Post-execution assessment (past-looking)
  - `plan_semaine_XX.md`: Action plan for the week (future-looking)
  - `R_HEBDO_S{WW}.md`: Weekly reference artifact summarizing decisions, indicators, and plans
- **Analysis files**: `data/phase{N}/S{WW}/analysis/a{X}.md`: intermediate analytical outputs

### Key Files & Their Purpose

| File | Purpose |
|------|---------|
| [project_registry.md](project_registry.md) | North star: finalité, objectives, constraints, current state |
| [workflows/cih/cih.md](workflows/cih/cih.md) | Complete CIH protocol definition |
| [roles/ps-*.md](roles) | Individual role specifications (9 files, one per role) |
| [activities](activities) | Activity definitions and registry |
| [workflows/cih/templates/](workflows/cih/templates) | Markdown templates for bilan/plan artifacts |
| `data/sleeping_history.csv` & `weight_history.csv` | Raw tracking data |

### Constraints to Preserve (Non-Negotiable)

From `project_registry.md`, these are hard constraints on recommendations:
- **Health priority**: No strategy should degrade sleep, recovery, or spinal health
- **Progressivity**: Don't increase exercise load + caloric deficit simultaneously  
- **Durability**: No extreme restrictions or compensatory behaviors
- **Signal priority**: Body signals (pain, fatigue, digestion) trump numbers
- **Target**: ~72 kg is a reference point, not an absolute goal

## The Primary Workflow: CIH (Cadre d'Itération Hebdomadaire)

When a user requests "run the CIH" or "execute the weekly iteration," this is the definitive workflow. 

**Authoritative source:** [workflows/cih/cih.md](workflows/cih/cih.md)

The CIH consists of 9 sequential steps, each governed by a specific cognitive role. Each role has its own detailed specification file in `roles/`.

### Invoking the CIH

When CIH is invoked, automatically load the workflow as defined in [cih.md](workflows/cih/cih.md).

Then proceed to **Step 1** as defined in [cih.md § 4](workflows/cih/cih.md#4-détail-par-étape).

### Understanding the 9 Steps

The complete CIH protocol is defined in [workflows/cih/cih.md](workflows/cih/cih.md):
- **Steps 1–5:** Analytical and framing roles (no decision)
- **Step 6:** Explicit human decision (mandatory, non-delegable)
- **Steps 7–9:** Planning, validation, and archival

**Do not paraphrase or invent step definitions.** Refer directly to [cih.md § 4](workflows/cih/cih.md#4-détail-par-étape) for:
- Exact inputs expected at each step
- Artifact names and locations
- Role boundaries and cognitive constraints
- Minimal required content for each artifact

### Step 6: Human Decision Point

The human decision point (Step 6) is mandatory and cannot be delegated. Present the outputs from Step 5 (`a5.md` as defined in [cih.md § 4.5](workflows/cih/cih.md#étape-5--ps-dir-07--orientation-stratégique-cadrée)) and await explicit user choice before proceeding to Step 7.

## Markdown Conventions & Project Patterns

This section documents observable patterns from the codebase. For formal definitions, consult the corresponding specification files.

### Markdown Conventions

- **Headings hierarchy**: H1 (title), H2 (major sections), H3 (subsections)
- **Metadata blocks**: Sections like "## Objectifs de la semaine" or "## Alimentation" appear consistently in weekly plans
- **Status notation**:
  - `RAS` = Rien À Signaler (no changes)
  - `→` = continuation or implication arrow
- **Activity naming**: Standard codes like `FB-30-BASE-V1` (Functional Base, 30 min, base level, version 1)
- **RPE scale**: 1–10 Borg Rating of Perceived Exertion; context-specific (e.g., 5–6 for moderate running)

### File Naming

- Phase files: `phase{N}.md` (N = 1, 2, 3, 4)
- Weekly files: `plan_semaine_{WW}.md` and `bilan_semaine_{WW}.md` (WW = week number)
- Analysis files: Sequential `a1.md`, `a2.md`, etc. under week's `analysis/` subdirectory
- Reference artifact: `R_HEBDO_Sxx.md` (weekly reference, created in Step 9)
- Templates: `template_*.md` in `workflows/cih/templates/`

## Key Principles

- **Single source of truth**: All data in CSV and markdown; no external APIs
- **Governance by design**: Every decision point is human-gated (Step 6 mandatory)
- **Role separation**: Each role has explicit boundaries; do not delegate decision-making across roles
- **Memory by design**: PS-SCR-06 (Step 9) maintains audit trail via `R_HEBDO_Sxx.md` and project registry updates

## When Uncertain, Consult

- **CIH protocol details**: [workflows/cih/cih.md](workflows/cih/cih.md) § 4
- **Role specifications**: The `roles/ps-*.md` file corresponding to the active step
- **Current project state**: [project_registry.md](project_registry.md)
- **Template structure**: Files in [workflows/cih/templates/](workflows/cih/templates/)
