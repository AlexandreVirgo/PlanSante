# A2_SIGNAUX_FAIBLES — Semaine 26

## Métadonnées
- **Semaine analysée** : S26
- **Période couverte** : 2 février – 8 février 2026
- **Rôle exécuteur** : PS-SIG-05 (Détection de signaux faibles)
- **Date génération** : 8 février 2026
- **Artefact source** : A1_ANALYSE_HEBDO.md
- **Données utilisateur brutes** : bilan_semaine_26.md, clarifications utilisateur post-A1

---

## 1. Cadre de détection

**Signaux détectés** : anomalies, variations anormales, dégradations, améliorations inhabituelles, écarts par rapport au plan ou à la baseline historique.

**Codification gravité** :
- 🔴 **Majeur** : impactant directement santé, performance, ou adhérence plan ; risque escalade court-terme
- 🟡 **Mineur** : déviation acceptable mais observable ; impactant indirectement ou long-terme
- 🟢 **Positif** : amélioration observable vs baseline ou attentes plan

**Certitude** : niveau d'incertitude sur étiologie (non diagnostic, pas d'attribution causale exclusive)

---

## 2. Signaux détectés S26

### 🔴 MAJEUR — Lombaire : signal transitoire associé à séance qualité

| Attribut | Valeur |
|----------|--------|
| **Description** | Signal lombaire émergent pendant RUN-TEMPO ; niveau de référence semaine montre un 2/4 le samedi soir |
| **Profil temporel** | Début semaine : matins 1–2 avec résolution intra-journée. Milieu semaine : RAS. Samedi : signal en séance + soir 2/4. Dimanche : retour 0 |
| **Contexte occurrence** | Séance tempo 46 min, RPE 6–7 (au-dessus cible), FC max 191 ; « rythme un peu élevé sur les 2 premiers blocs » |
| **Clarification utilisateur** | Apparition légère au **bloc 2**, puis **montée progressive** sur les blocs 3–4 jusqu’à **2/4** ; **lendemain matin 0/4** |
| **Novité vs S25** | Profil plus “événementiel” (lié à une séance) vs S25 (escalade fin de semaine plus diffuse/persistante) |
| **Hypothèses étiologiques (sans diagnostic)** | (1) Intensité/rythme trop élevé au départ → compensation posturale ; (2) charge mécanique (surface/dénivelé) ; (3) fatigue stabilisateurs lombaires malgré modulation ; (4) technique (foulée, gainage, amplitude) |
| **Certitude étiologie** | **Moyenne** : association temporelle + marqueurs (RPE/FC) + signal en séance. Causalité exacte non démontrée |
| **Risque escalade court-terme** | **Faible–modéré** : signal transitoire (retour à 0 le lendemain) mais répétition si intensité dérive |
| **Indicateur de santé menacé** | OUI : contrainte non négociable « santé lombaire » ([project_registry.md](/project_registry.md)) |

---

### 🟡 MINEUR — Genou gauche : signal léger en EF

| Attribut | Valeur |
|----------|--------|
| **Description** | Léger signal genou gauche pendant ou autour de RUN-40-EF |
| **Profil temporel** | Isolé (rapporté sur la séance EF), absent sur la séance tempo |
| **Contexte occurrence** | EF 35 min, RPE 3, allure lente 9:06/km, FC moy 141 |
| **Clarification utilisateur** | Localisation **côté extérieur** ; **disparaît totalement après** ; intuition utilisateur : apparaît surtout quand l’allure est très lente (répétition/amplitude) |
| **Novité vs S25** | S25 : RAS genou. S26 : réapparition légère |
| **Hypothèses étiologiques (sans diagnostic)** | (1) variabilité terrain/chaussures ; (2) fatigue locale ; (3) mécanique de course (cadence/attaque) ; (4) enchaînement semaine |
| **Certitude** | **Moyenne** : signal qualifié (latéral externe, transitoire), mais sans données biomécaniques |
| **Risque escalade** | **Faible** si reste isolé ; à surveiller si répétitif |

---

### 🟡 MINEUR — Dérive de la séance tempo vs cible (intensité/volume)

| Attribut | Valeur |
|----------|--------|
| **Description** | Tempo réalisé avec intensité perçue et biométrie plus hautes que la cible (RPE 6–7 vs 6 ; FC max 191) et durée 46 min vs 40 min |
| **Profil temporel** | Constat sur la séance ; auto-correction en séance (2 derniers blocs plus adaptés) |
| **Lien avec signaux** | Coïncide avec signal lombaire pendant séance |
| **Certitude** | **Moyenne–haute** : données rapportées précises |
| **Risque escalade** | **Faible–modéré** : si pattern “départ trop vite” se répète, augmente probabilité de signaux mécaniques |

---

### 🟡 MINEUR — Sommeil : gain porté par week-end (couchers tardifs choisis)

| Attribut | Valeur |
|----------|--------|
| **Description** | Sommeil moyen en forte hausse, mais avec deux couchers tardifs (00:34, 01:17) **choisis** et levers tardifs week-end |
| **Profil temporel** | Semaine : plusieurs nuits ~7h00 ; week-end : 10h29 et 7h59 avec couchers tardifs |
| **Clarification utilisateur** | Week-end sans contrainte, couchers tardifs volontairement choisis ; pas de ressenti net de dette de sommeil. Pattern semaine/week-end structurel : lever semaine ~6h, et préférence de ne pas se coucher avant ~23h |
| **Certitude** | **Haute** : données + clarification |
| **Risque escalade** | **Faible** (si compatible vie) ; **incertitude** sur transférabilité en semaine contrainte |

---

### 🟢 POSITIF — Sommeil : objectif dépassé nettement

| Attribut | Valeur |
|----------|--------|
| **Description** | Moyenne 7h41 (vs 7h11 S25) = +30 min ; objectif >7h10 atteint |
| **Certitude** | **Haute** (sleeping_history.csv + Sommeil.csv cohérents) |
| **Impact positif** | Améliore marges de récupération neuromusculaire, surtout en fin de phase de déficit |

---

### 🟢 POSITIF — Adhérence plan & modulation : 3/3 séances, durées modulées respectées

| Attribut | Valeur |
|----------|--------|
| **Description** | 3/3 séances réalisées ; FB et EF respectent les durées modulées ; spacing lun/jeu/sam respecté |
| **Certitude** | **Haute** |
| **Impact positif** | Confirme capacité d’exécuter un plan modulé prudent (objectif central S26) |

---

### 🟢 POSITIF — État psycho-physio global stable

| Attribut | Valeur |
|----------|--------|
| **Description** | Énergie bonne, motivation bonne, humeur positive, digestion RAS |
| **Certitude** | **Moyenne** (autoreport, mais cohérent) |

---

## 3. Tableau synthétique signaux S26

| Gravité | Signal | Profil | Certitude étiologie | Risque escalade |
|---------|--------|--------|-------------------|-----------------|
| 🔴 Majeur | Lombaire en séance tempo (pic 2/4) + samedi soir 2/4 | Transitoire, lié séance | Moyenne | Faible–modéré |
| 🟡 Mineur | Genou G léger (EF) | Isolé | Basse–moyenne | Faible |
| 🟡 Mineur | Dérive tempo (RPE/FC/durée) | Départ trop vite puis correction | Moyenne–haute | Faible–modéré |
| 🟡 Mineur | Sommeil porté par week-end (couchers tardifs choisis) | Gain réel mais contexte | Haute | Faible |
| 🟢 Positif | Sommeil +30 min | Objectif dépassé | Haute | Basse |
| 🟢 Positif | Adhérence plan modulé (3/3) | Spacing + durées ok | Haute | Basse |
| 🟢 Positif | Énergie/motivation/humeur/digestion stables | Autoreport stable | Moyenne | Basse |

---

## 4. Incertitudes documentées

1. **Causalité exacte lombaire pendant tempo** : association temporelle forte (apparition au bloc 2), mais variables non observées (terrain, technique, échauffement, fatigue pré-séance).
2. **Genou gauche** : signal qualifié (latéral externe, transitoire) mais facteurs déclenchants exacts incertains (allure lente, amplitude, chaussures, surface).
3. **Sommeil** : amélioration réelle, mais une partie provient de la flexibilité week-end ; à vérifier en semaine contrainte (stabilisation).

---

## 5. Questions pour utilisateur (optionnel)

Répondre si tu as 2–3 min. Sinon, tape "continuer" pour Étape 3.

1. Sur la séance tempo : tu confirmes apparition au **bloc 2**. Est-ce que le signal est resté stable (≈2/4) ou est-ce qu’il a augmenté sur les blocs 3–4 ?
2. Genou G : tu confirmes **côté extérieur** et disparition post-séance. Est-ce que ça se manifeste aussi à des allures plus rapides, ou uniquement à très lent ?
3. Pattern semaine/week-end : en semaine (lever ~6h) tu préfères ne pas te coucher avant ~23h. En stabilisation, tu vises plutôt à **protéger la durée** (lever fixe, coucher pareil) ou à accepter une **durée plus courte en semaine** compensée week-end ?