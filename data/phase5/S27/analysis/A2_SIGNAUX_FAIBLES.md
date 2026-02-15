# A2_SIGNAUX_FAIBLES — Semaine 27

## Métadonnées
- **Semaine analysée** : S27
- **Période couverte** : 9 février 2026 – 15 février 2026
- **Phase active** : Phase 5 (stabilisation structurée)
- **Rôle exécuteur** : PS-SIG-05 (Détection de signaux faibles)
- **Date génération** : 15 février 2026
- **Artefact source** : A1_ANALYSE_HEBDO.md
- **Données utilisateur brutes** : bilan_semaine_27.md + clarifications post-A1

---

## 1. Cadre de détection

**Signaux détectés** : anomalies, variations, ruptures, améliorations inhabituelles, écarts par rapport au plan ou à la baseline.

**Codification gravité** :
- 🔴 **Majeur** : impact direct santé / risque escalade court-terme / contrainte non négociable menacée
- 🟡 **Mineur** : déviation observable mais tolérable ; impact indirect ou long-terme
- 🟢 **Positif** : amélioration ou stabilité notable vs baseline / attentes plan

**Certitude** : niveau d’incertitude sur l’étiologie (pas de diagnostic, pas d’attribution causale unique).

---

## 2. Signaux détectés S27

### 🟡 MINEUR — Sommeil : objectif “coucher 22h30/23h” non atteint (objectif déclaré comme idéal)

| Attribut | Valeur |
|----------|--------|
| **Description** | Objectif Phase 5 / plan S27 : coucher 22h30/23h la majorité des nuits. Données S27 : coucher moyen consolidé 23:56, et 0 nuit ≤ 23:00 (Sommeil.csv). Clarification : objectif qualifié comme **idéal**, la **durée** prime. |
| **Profil temporel** | Couchers tardifs constants ; week-end très tard (01:00, 01:14), confirmés comme **choisis** |
| **Niveau d’incertitude** | **Faible** : données chiffrées + clarification utilisateur |
| **Risque escalade** | **Faible** : durée actuelle correcte (~7h38) et pas d’effet négatif notable rapporté ; risque si contraintes de lever augmentent (réduction de durée) |
| **Indicateur menacé** | Partiel : indicateur “Sommeil” retenu (cible coucher), mais priorité utilisateur = **durée** |

---

### 🟡 MINEUR — Poids : hausse rapide vs S26 (transition Phase 4 → Phase 5)

| Attribut | Valeur |
|----------|--------|
| **Description** | Poids moyen calculé S27 76.16 kg vs S26 75.43 kg : **+0.73 kg** |
| **Profil temporel** | Pic 77.0 kg le 09/02, dans un contexte week-end familial ; pesée standard (matin à jeun après selle) |
| **Hypothèses étiologiques (sans diagnostic)** | (1) retour glycogène/eau post-diète ; (2) sel/repas plus riches ; (3) transit ; (4) variabilité normale |
| **Certitude étiologie** | **Moyenne** (contexte plausible, mais indistinguable d’un gain réel sans série plus dense) |
| **Risque escalade** | **Faible** à court terme ; à surveiller si le palier continue de monter sur 10–14 jours |

---

### 🟡 MINEUR — Running EF : dérive d’intensité cardio vs cible (ou zones mal calibrées)

| Attribut | Valeur |
|----------|--------|
| **Description** | EF jeudi : RPE 4–5 mais FC moy 158, max 174 + ~50% zone 3 / 50% zone 4 (zones montre). EF dimanche ajoutée : FC moy 145, max 165, majoritairement zone 3 |
| **Contexte** | Zones basées sur % de FC max avec FC max **estimée** (observations anciennes), sans test formel |
| **Niveau d’incertitude** | **Élevé** : l’alerte peut refléter soit (a) une intensité cardio réellement trop haute, soit (b) des zones mal calibrées, soit (c) capteur / conditions |
| **Risque escalade** | **Faible–modéré** : si EF devient “trop soutenue”, peut augmenter fatigue globale et interagir avec objectif lombaire/sommeil |

---

### 🟡 MINEUR — Charge hebdo : séance non prévue ajoutée

| Attribut | Valeur |
|----------|--------|
| **Description** | 3/3 séances prévues réalisées + ajout RUN-50-EF le dimanche |
| **Profil temporel** | Ajout en fin de semaine (après fartlek samedi) |
| **Certitude** | **Haute** (bilan) |
| **Risque escalade** | **Faible** sur S27 (signaux RAS), mais constitue un pattern possible de “volume ↑” qui peut entrer en tension avec l’objectif de stabilisation / sommeil |

---

### 🟡 MINEUR — Lombaire : micro-signal (raideur) en fin d’EF

| Attribut | Valeur |
|----------|--------|
| **Description** | Raideur lombaire légère en fin de séance EF jeudi, sans douleur |
| **Certitude** | **Moyenne** (qualitatif) |
| **Risque escalade** | **Faible** (pas de persistance / RAS ailleurs), mais à noter car la lombaire est une contrainte non négociable |

---

### 🟢 POSITIF — Signaux corporels : genou et lombaire globalement RAS

| Attribut | Valeur |
|----------|--------|
| **Description** | Aucun signal genou reporté ; lombaire globalement RAS (hors raideur légère isolée) |
| **Certitude** | **Moyenne–haute** (autoreport cohérent sur plusieurs séances) |
| **Impact positif** | Confirme une tolérance correcte de la semaine 1/4 en Phase 5 |

---

### 🟢 POSITIF — Adhérence : plan S27 exécuté

| Attribut | Valeur |
|----------|--------|
| **Description** | 3/3 séances planifiées réalisées, consignes nutrition globalement respectées |
| **Certitude** | **Haute** |

---

## 3. Tableau synthétique signaux S27

| Gravité | Signal | Profil | Incertitude étiologie | Risque escalade |
|---------|--------|--------|----------------------|-----------------|
| 🟡 Mineur | Coucher trop tard vs objectif Phase 5 (objectif idéal) | Pattern semaine + week-end tardif choisi | Basse | Faible |
| 🟡 Mineur | Poids +0.73 kg vs S26 | Transition + week-end | Moyenne | Faible |
| 🟡 Mineur | EF “trop en zones hautes” ou zones mal calibrées | Répété sur 2 EF | Élevée | Faible–modéré |
| 🟡 Mineur | Séance ajoutée (volume ↑) | Ajout dimanche | Basse | Faible |
| 🟡 Mineur | Raideur lombaire légère EF | Isolé | Moyenne | Faible |
| 🟢 Positif | Lombaire/genou globalement RAS | Stable | Moyenne | Basse |
| 🟢 Positif | Adhérence plan | 3/3 réalisées | Basse | Basse |

---

## 4. Incertitudes documentées

1. **Zones FC** : calibration (FC max estimée) et/ou capteur peuvent biaiser la lecture “Z3/Z4”.
2. **Poids** : variabilité hydrique post-transition vs gain réel non distinguables sans plus de points de mesure.
3. **Sommeil** : durée actuelle bonne malgré couchers tardifs ; risque dépend de la contrainte de lever (non observée ici).

---

## 5. Questions pour utilisateur (optionnel)

Répondre si tu as 2–3 min. Sinon, tape "continuer" pour Étape 3.

1. Sur l’objectif coucher 22h30/23h : est-ce un **objectif réellement prioritaire** pour toi en Phase 5, ou plutôt un “idéal” (avec acceptation d’un coucher ~23h30–00h si durée OK) ?
2. Les deux nuits très tardives (01:00, 01:14) : est-ce que ça a eu un **effet le lendemain** (somnolence, irritabilité, envie de sucre, motivation sport) ou RAS ?
3. Sur l’EF : tu utilises plutôt le **talk test / sensation facile** ou tu cherches à suivre strictement la zone FC (même si elle semble mal calibrée) ?

---

## 6. Intégration du feedback utilisateur (Clarifications Étape 2)

### Réponses utilisateur intégrées

**Q1 — Objectif coucher 22h30/23h** : qualifié comme **idéal**, la **durée** prime. → Le signal est conservé (écart à l’objectif formel), mais requalifié en **mineur** car il n’est pas une priorité stricte tant que la durée et l’état diurne restent stables.

**Q2 — Effet des couchers tardifs** : **RAS** le lendemain (fatigue/humeur/envies). → Réduit le risque court-terme associé.

**Q3 — Pilotage EF** : pilotage aux **sensations**, mais les objectifs FC perturbent ; intention de reconfigurer la montre pour des blocs **libres** (non basés FC). → Diminue le risque de sur-contrainte cognitive liée aux zones, et rend l’interprétation des zones FC plus “diagnostique” que prescriptive.

### Synthèse après clarifications
Les signaux “sommeil” et “zones FC” restent présents comme écarts/incohérences observables, mais :
- le sommeil est plutôt un **choix de routine** compatible (pour l’instant) avec une bonne durée,
- la FC en zones hautes est davantage un **signal incertain de calibration** qu’un signal ferme d’intensité excessive.
