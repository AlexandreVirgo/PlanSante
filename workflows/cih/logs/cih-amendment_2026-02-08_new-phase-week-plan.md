# CIH AMENDMENT — 2026-02-08
## Correctif : création de nouvelle phase ⇒ génération du plan semaine + persistance phase précédente

**Date** : 8 février 2026  
**Contexte** : Exécution CIH S26 → création Phase 5 à l'étape 7, mais absence de plan hebdomadaire pour la première semaine de la nouvelle phase.

---

## 1. Problème constaté
Quand la décision humaine entraîne la **création d'une nouvelle phase**, la procédure CIH (v3) ne spécifiait pas la production du **plan de la semaine à venir** dans cette nouvelle phase.

Conséquence : on obtient `phase{N+1}.md`, mais pas `/data/phase{N+1}/S{WW+1}/plan_semaine_{WW+1}.md`.

---

## 2. Décision
- Le **plan hebdomadaire** de la semaine suivante doit être **produit dans tous les cas**.
- En cas de création d'une nouvelle phase, l'étape 7 doit produire **deux artefacts de planification** :
  - la **nouvelle phase** (`phase{N+1}.md`)
  - le **plan de la première semaine** de cette phase (`S{WW+1}/plan_semaine_{WW+1}.md`)
- La persistance (étape 9) doit aussi mettre à jour la **phase précédente** pour refléter la transition/clôture actée.

---

## 3. Changements effectués
### A. Étape 7 — PS-PLAN-08
- Le `plan_semaine_{WW+1}.md` est rendu **obligatoire dans tous les cas**.
- En cas de nouvelle phase : création **en plus** du fichier `phase{N+1}.md`.

### B. Étape 9 — PS-SCR-06
- Ajout d'un cas explicite “création d'une nouvelle phase” :
  - mise à jour de `/data/phase{N}/phase{N}.md` (phase précédente)
  - mise à jour de `/data/phase{N+1}/phase{N+1}.md` (nouvelle phase)
  - mise à jour de `/project_registry.md`

---

## 4. Fichiers modifiés
- [workflows/cih/cih.md](workflows/cih/cih.md)

---

## 5. Notes
- Aucun changement demandé/nécessaire aux templates.
- Aucun changement aux rôles cognitifs.
