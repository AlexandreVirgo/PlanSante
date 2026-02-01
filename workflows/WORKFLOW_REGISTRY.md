# Workflow Registry

This registry documents all executable workflows in the AIProjectFramework.

## How to Use This Registry

When a user requests to execute or resume a workflow, match their request against the table below:
- **Keywords** are case-insensitive and support linguistic variants
- **File** points to the authoritative workflow definition
- **Entry Point** specifies where to begin (Étape 1 for fresh start, or Étape N for resume)
- **Primary Role** is the cognitive posture the agent adopts during execution
- **Purpose** describes what the workflow accomplishes

---

## Available Workflows

| Workflow | Keywords (any variant) | File | Entry Point | Primary Role | Purpose |
|----------|------------------------|------|-------------|--------------|---------|
| **CORAL-P** | initialize project, setup registry, start coral-p, run coral-p, execute coral-p, launch coral-p | `workflows/coral-p/coral-p.md` | § 4, Étape 1 | META-GOV-01 | Initialize and iteratively build the project registry through structured clarification of finalité, objectifs, contraintes, hypothèses, and indicateurs |
| **CORAL-P Resume** | resume coral-p, continue coral-p, reprise coral-p, reprendre coral-p [at/from/à/à l'étape] N | `workflows/coral-p/coral-p.md` | § 4, Étape N | META-GOV-01 | Resume CORAL-P from a specific step (N = step number between 1 and 8) |
| **IRIS-R** | identify roles, define roles, rationalize roles, run iris-r, execute iris-r, launch iris-r | `workflows/iris-r/iris-r.md` | § 4, Étape 1 | META-GOV-01 | Identify and rationalize cognitive roles needed for the project based on project registry and cognitive needs |
| **IRIS-R Resume** | resume iris-r, continue iris-r, reprise iris-r, reprendre iris-r [at/from/à/à l'étape] N | `workflows/iris-r/iris-r.md` | § 4, Étape N | META-GOV-01 | Resume IRIS-R from a specific step (N = step number between 1 and 6) |
| **CIH** | execute cih, run cih, launch cih, start cih | `workflows/cih/cih.md` | § 4, Étape 1 | Varies by step | Execute the Cadre d'Itération Humaine (CIH) workflow for project planning and execution |
| **CIH Resume** | resume cih, continue cih, reprise cih, reprendre cih [at/from/à/à l'étape] N | `workflows/cih/cih.md` | § 4, Étape N | Varies by step | Resume CIH from a specific step (N = step number between 1 and 9) |

---


