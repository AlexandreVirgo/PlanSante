# CADRE D’ITÉRATION HEBDOMADAIRE (CIH)
## Plan de santé personnalisé

---

## 1. Objet du cadre

Le **Cadre d’Itération Hebdomadaire (CIH)** définit un protocole réutilisable
d’actionnement séquentiel des rôles cognitifs du projet.

Il vise à :
- conduire le projet dans le temps de manière structurée,
- garantir la comparabilité inter-semaines,
- préserver la gouvernance humaine,
- produire une mémoire exploitable du plan.

Ce cadre :
- **ne décide pas**,
- **ne prescrit pas**,
- **n’automatise aucune action**.

---

## 2. Principes généraux

- Un seul rôle est actif à la fois.
- Chaque rôle :
  - consomme des **inputs explicitement définis**,
  - produit **un artefact identifié**.
- Les artefacts sont classés en :
  - **intermédiaires** (non persistés),
  - **de référence** (persistés après décision humaine).
- La **décision humaine** est un point explicite du cadre.
- La mémoire du système est assurée **exclusivement par PS-SCR-06**.

---

## 3. Séquence hebdomadaire standard

### Vue d’ensemble

1. PS-ANA-02 — Analyse factuelle
2. PS-SIG-05 — Détection de signaux faibles
3. PS-COH-04 — Contrôle de cohérence
4. PS-STR-01 — Structuration des constats
5. PS-DIR-07 — Orientation stratégique cadrée
6. **Décision humaine**
7. PS-SCR-06 — Persistance et traçabilité

---

## 4. Détail par rôle

---

### Étape 1 — PS-ANA-02 : Analyse du bilan hebdomadaire

**Inputs attendus**
- Registre de projet (version courante)
- Phase en cours
- Plan de la semaine écoulée
- Bilan hebdomadaire utilisateur
- Données historiques pertinentes (poids, sommeil, charge)

**Artefact produit (intermédiaire)**
- `A1_ANALYSE_HEBDO.md`

**Contenu minimal**
- Tendances observées
- Comparaison avec semaines précédentes
- Variations notables
- Hypothèses et biais signalés

---

### Étape 2 — PS-SIG-05 : Signaux faibles

**Inputs attendus**
- `A1_ANALYSE_HEBDO.md`
- Bilan brut utilisateur (ressenti, fatigue, irritants)

**Artefact produit (intermédiaire)**
- `A2_SIGNAUX_FAIBLES.md`

**Contenu minimal**
- Liste de signaux détectés
- Niveau d’incertitude associé
- Absence de conclusion ou diagnostic

---

### Étape 3 — PS-COH-04 : Contrôle de cohérence

**Inputs attendus**
- Registre de projet
- Phase en cours
- Plan de la semaine écoulée
- `A1_ANALYSE_HEBDO.md`
- `A2_SIGNAUX_FAIBLES.md`

**Artefact produit (intermédiaire)**
- `A3_COHERENCE.md`

**Contenu minimal**
- Incohérences potentielles identifiées
- Tensions entre objectifs, contraintes et pratiques
- Aucun jugement d’opportunité

---

### Étape 4 — PS-STR-01 : Structuration des constats

**Inputs attendus**
- `A1_ANALYSE_HEBDO.md`
- `A2_SIGNAUX_FAIBLES.md`
- `A3_COHERENCE.md`

**Artefact produit (intermédiaire)**
- `A4_SYNTHESE_STRUCTUREE.md`

**Contenu minimal**
- État synthétique de la semaine
- Tensions structurantes
- Questions ouvertes
- Cadres formels mobilisables

---

### Étape 5 — PS-DIR-07 : Orientation stratégique cadrée

**Inputs attendus**
- Registre de projet
- Phase en cours
- `A4_SYNTHESE_STRUCTUREE.md`

**Artefact produit (intermédiaire)**
- `A5_OPTIONS_STRATEGIQUES.md`

**Contenu minimal**
- 2 à 4 options de trajectoire plausibles
- Conditions de poursuite / prolongement / clôture de phase
- Implications et risques
- Points de décision explicitement laissés à l’humain

---

## 5. Point de décision humaine (obligatoire)

À partir de `A5_OPTIONS_STRATEGIQUES.md`, l’humain décide explicitement :
- de l’état de la phase :
  - poursuite,
  - prolongement,
  - clôture,
- du plan de la semaine suivante,
- de la création éventuelle d’une nouvelle phase.

Aucune décision n’est implicite.
Aucun rôle cognitif ne valide ce choix.

---

## 6. Étape finale — PS-SCR-06 : Persistance et mémoire

**Inputs attendus**
- Décision humaine explicitée
- Artefacts intermédiaires validés

**Artefacts de référence produits**
- `R_HEBDO_Sxx.md` — Synthèse hebdomadaire validée
- Mise à jour de :
  - l’état de la phase,
  - du plan de la semaine suivante,
  - du registre de projet (si nécessaire)

**Règle**
- PS-SCR-06 ne reformule pas.
- PS-SCR-06 ne synthétise pas.
- PS-SCR-06 documente fidèlement.

---

## 7. Artefacts et persistance

### Artefacts intermédiaires (non persistés)
- A1_ANALYSE_HEBDO
- A2_SIGNAUX_FAIBLES
- A3_COHERENCE
- A4_SYNTHESE_STRUCTUREE
- A5_OPTIONS_STRATEGIQUES

### Artefacts de référence (persistés)
- R_HEBDO_Sxx
- Registre de projet (versionné)
- Phase en cours (état mis à jour)
- Plan hebdomadaire

---

## 8. Statut du cadre

- **Statut** : stabilisé
- **Révision** : uniquement via décision humaine
- **Évolution** : via IRIS-R si nécessaire

---

## 9. Rappel de gouvernance

- Aucun rôle ne décide.
- Aucun rôle ne valide.
- L’humain conserve le contrôle effectif du projet.

Ce cadre vise à **aider à penser et à piloter**, non à automatiser.
