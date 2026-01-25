# CADRE D’ITÉRATION HEBDOMADAIRE (CIH)
## Plan de santé personnalisé — Version étendue

---

## 1. Objet du cadre

Le **Cadre d’Itération Hebdomadaire (CIH)** définit un protocole réutilisable
d’actionnement séquentiel des rôles cognitifs du projet.

Il vise à :
- conduire le projet dans le temps de manière structurée,
- garantir la comparabilité inter-semaines,
- préserver la gouvernance humaine,
- produire une mémoire exploitable du plan,
- rendre le projet **opérationnel** (plans concrets).

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
- La **décision humaine** est un point explicite et non contournable.
- La mémoire du système est assurée **exclusivement par PS-SCR-06**.
- Aucun rôle ne valide le travail d’un autre rôle.

---

## 3. Séquence hebdomadaire standard (vue d’ensemble)

1. PS-ANA-02 — Analyse factuelle  
2. PS-SIG-05 — Détection de signaux faibles  
3. PS-COH-04 — Contrôle de cohérence (amont)  
4. PS-STR-01 — Structuration des constats  
5. PS-DIR-07 — Orientation stratégique cadrée  
6. **Décision humaine explicite**  
7. PS-PLAN-08 — Plan concret (opérationnalisation)  
8. PS-COH-04 — Contrôle de cohérence (aval, optionnel)  
9. PS-SCR-06 — Persistance et traçabilité  

---

## 4. Détail par étape

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
- Comparaisons temporelles
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
- Absence de diagnostic ou conclusion

---

### Étape 3 — PS-COH-04 : Contrôle de cohérence (amont)

**Inputs attendus**
- Registre de projet
- Phase en cours
- Plan de la semaine écoulée
- `A1_ANALYSE_HEBDO.md`
- `A2_SIGNAUX_FAIBLES.md`

**Artefact produit (intermédiaire)**
- `A3_COHERENCE_AMONT.md`

**Contenu minimal**
- Incohérences potentielles
- Tensions logiques identifiées
- Aucun jugement d’opportunité

---

### Étape 4 — PS-STR-01 : Structuration des constats

**Inputs attendus**
- `A1_ANALYSE_HEBDO.md`
- `A2_SIGNAUX_FAIBLES.md`
- `A3_COHERENCE_AMONT.md`

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
- **Option 0 : continuité stricte** (par défaut)
- 1 à 3 options alternatives
- Conditions, implications, risques
- Décision explicitement laissée à l’humain

---

## 5. Décision humaine explicite (obligatoire)

À partir de `A5_OPTIONS_STRATEGIQUES.md`, l’humain décide explicitement :
- de l’état de la phase (poursuite / prolongement / clôture),
- de l’option stratégique retenue,
- du périmètre du plan suivant (hebdomadaire ou phase).

Aucune décision n’est implicite.  
Aucun rôle cognitif ne valide ce choix.

---

### Étape 6 — PS-PLAN-08 : Plan concret (opérationnalisation)

**Inputs attendus**
- Décision humaine explicite
- Phase en cours ou nouvelle phase validée
- Registre de projet
- Contraintes non négociables

**Artefact produit (intermédiaire)**
- `A6_PLAN_CONCRET.md`

**Règles impératives**
- Le plan généré respecte strictement :
  - `template_plan_semaine.md` **ou**
  - `template_phase.md`
- Aucune adaptation du template
- Aucune alternative stratégique proposée

---

### Étape 7 — PS-COH-04 : Contrôle de cohérence (aval, optionnel)

**Objectif**
Vérifier que le plan concret :
- respecte le registre,
- ne viole aucune contrainte non négociable,
- est cohérent avec la décision humaine.

**Inputs attendus**
- Décision humaine
- `A6_PLAN_CONCRET.md`
- Registre de projet

**Artefact produit (intermédiaire, optionnel)**
- `A7_COHERENCE_EX_POST.md`

**Règle**
- Aucun blocage
- Aucun arbitrage
- Signalement uniquement

---

### Étape 8 — PS-SCR-06 : Persistance et mémoire

**Inputs attendus**
- Décision humaine
- Plan concret validé
- Éventuel contrôle de cohérence ex post

**Artefacts de référence produits**
- `R_HEBDO_Sxx.md`
- Mise à jour :
  - du plan hebdomadaire,
  - de l’état de la phase,
  - du registre de projet (si requis)

**Règle**
- Documentation fidèle
- Aucune interprétation

---

## 6. Artefacts et persistance

### Artefacts intermédiaires
- A1_ANALYSE_HEBDO
- A2_SIGNAUX_FAIBLES
- A3_COHERENCE_AMONT
- A4_SYNTHESE_STRUCTUREE
- A5_OPTIONS_STRATEGIQUES
- A6_PLAN_CONCRET
- A7_COHERENCE_EX_POST (optionnel)

### Artefacts de référence
- R_HEBDO_Sxx
- Registre de projet versionné
- Plan hebdomadaire ou phase active

---

## 7. Statut du cadre

- **Statut** : stabilisé (CIH v2)
- **Révision** : décision humaine uniquement
- **Évolution** : via IRIS-R

---

## 8. Rappel de gouvernance

- Aucun rôle ne décide.
- Aucun rôle ne valide.
- Le cadre structure, l’humain gouverne.

Ce CIH vise à rendre le projet **pensable, pilotable et applicable** dans la durée.
