# A1_ANALYSE_HEBDO — Semaine 26

## Métadonnées
- **Semaine analysée** : S26
- **Période couverte** : 2 février – 8 février 2026
- **Rôle exécuteur** : PS-ANA-02 (Analyse factuelle)
- **Date génération** : 8 février 2026
- **Artefacts sources** : bilan_semaine_26.md, plan_semaine_26.md, weight_history.csv, sleeping_history.csv, Sommeil.csv, R_HEBDO_S25.md

---

## 1. Analyse pondérale

### Données brutes S26 (weight_history.csv)
- 2026-02-03 : 75.3 kg
- 2026-02-05 : 76.0 kg
- 2026-02-06 : 75.4 kg
- 2026-02-07 : 75.0 kg

**Poids moyen S26 (calculé sur points disponibles)** : **75.43 kg** (n=4)

### Comparaison temporelle S25 → S26
- **Poids moyen S25 (calculé)** : **75.62 kg** (n=5, du 27 jan au 1 fév)
- **Poids moyen S26 (calculé)** : **75.43 kg** (n=4, du 3 fév au 7 fév)
- **Variation S25→S26** : **-0.20 kg**

**Observation clé** : La trajectoire reste cohérente avec l’objectif Phase 4 « palier bas ~75–75.5 kg ». La baisse est faible mais présente, compatible avec une fin de phase (palier + bruit hydrique) et avec un week-end plus copieux rapporté.

---

## 2. Analyse sommeil

### Données consolidées S26 (sleeping_history.csv)
- **Sommeil moyen S26** : **7h 41m**
- **Heure de coucher moyenne S26** : **11:48 PM**
- **Heure de lever moyenne S26** : **7:34 AM**

### Comparaison temporelle S25 → S26 (sleeping_history.csv)
- **Sommeil moyen S25** : 7h 11m
- **Sommeil moyen S26** : 7h 41m
- **Variation S25→S26** : **+30 min**
- **Coucher moyen** : 11:43 PM → 11:48 PM (**+5 min**, légèrement plus tard)
- **Lever moyen** : 6:57 AM → 7:34 AM (**+37 min**)

**Observation clé** : L’objectif S26 « > 7h10 (non négociable) » est atteint nettement. L’amélioration vient surtout d’un lever plus tardif en moyenne (et d’une nuit très longue), plus que d’un coucher avancé.

### Données quotidiennes S26 (Sommeil.csv)
| Date | Durée | Coucher | Lever |
|------|-------|---------|-------|
| 2026-02-02 | 7h 23m | 11:37 PM | 7:00 AM |
| 2026-02-03 | 7h 00m | 11:12 PM | 6:22 AM |
| 2026-02-04 | 7h 07m | 11:14 PM | 6:25 AM |
| 2026-02-05 | 7h 00m | 11:21 PM | 6:27 AM |
| 2026-02-06 | 6h 52m | 11:26 PM | 6:18 AM |
| 2026-02-07 | 10h 29m | 12:34 AM | 11:11 AM |
| 2026-02-08 | 7h 59m | 1:17 AM | 9:20 AM |

**Durée moyenne calculée (7 jours)** : **7h 41m** (cohérent sleeping_history.csv)

**Notes factuelles** :
- 1 nuit < 7h (6h52 le 06/02)
- 1 nuit très longue (10h29 le 07/02) = probable récupération/compensation
- Deux couchers tardifs notables : 00:34 (07/02), 01:17 (08/02)

---

## 3. Analyse activités physiques

### Conformité plan S26 (Option 1 — modulation préemptive prudente)

| Activité planifiée | Statut | Notes factuelles |
|-------------------|--------|------------------|
| FB-30-BASE-V1 (Lundi, 20–25 min, RPE 5–6) | ✓ Complétée | RPE 5. Séries réduites (modulation appliquée). Pont fessier +2 séries. FC max 139. Aucun signal lombaire/genou en séance. |
| RUN-40-EF-V1 (Jeudi, 35 min, RPE 3–4) | ✓ Complétée | 35 min (modulation appliquée). Allure 9:06/km. FC moy 141, max 161. RPE 3. Léger signal genou G + léger signal lombaire. |
| RUN-40-TEMPO-FRACTIONNE-V1 (Samedi, 40 min, RPE 6) | ✓ Complétée | 46 min (un peu > plan). RPE 6–7 (au-dessus de la cible). FC moy 164, max 191. 4 blocs réalisés ; 2 premiers trop rapides, 2 derniers plus adaptés. Signal lombaire émergent milieu de séance, montant sur les 2 derniers blocs (≈2/4). |

**Conformité globale** : **3/3 séances réalisées**. La modulation « réduction cumul / spacing » est respectée (lun/jeu/sam), et les réductions de durée sont respectées sur FB et EF. La séance qualité est réalisée mais avec une intensité perçue > cible.

---

## 4. Analyse signaux corporels — Lombaire (prioritaire)

### Données brutes S26 (échelle 0–4)
- Lundi : matin 1, soir 0
- Mardi : matin 2, soir 0
- Mercredi : matin 1, midi 0
- Jeudi : matin 0, soir 0
- Vendredi : 0
- Samedi : matin 0, soir 2
- Dimanche : 0

### Profil temporel
- **Début de semaine** : résidu léger (matins 1–2) avec résolution intra-journée.
- **Fin de semaine** : **réapparition niveau 2** le samedi soir, concomitante à une séance qualité rapportée comme plus intense que prévu et avec signal lombaire en séance.

### Comparaison factuelle S25 → S26
- S25 : escalade niveau 2 sam–dim (persistante fin de semaine, cause incertaine)
- S26 : niveau 2 réapparaît samedi soir mais avec un **événement déclencheur plus plausible** (séance tempo, RPE 6–7, FC max 191, signal lombaire en séance)

**Observation clé** : La modulation semble avoir stabilisé le milieu de semaine (jeudi/vendredi RAS), mais la séance qualité reste un point de fragilité mécanique (lombaire) si l’intensité dépasse la cible.

---

## 5. Autres signaux corporels

### Genou gauche
- Mentionné comme **léger signal** sur la séance EF (jeudi).
- **Aucun signal genou** reporté sur la séance tempo (samedi).

### Énergie / motivation / humeur / digestion
- **Énergie** : bonne
- **Motivation** : bonne
- **Humeur** : positive
- **Digestion** : RAS
- **Sommeil (qualitatif)** : “correct” (bilan), et quantitativement en nette hausse.

---

## 6. Analyse nutrition — Phase 4

### Adhérence rapportée
- **Consignes** : respectées.
- Semaine : repas alignés recommandations.
- Week-end : événement familial avec repas plus copieux.

**Observation clé** : Pas de signal de dérive majeure ; la stabilité/ baisse pondérale reste cohérente malgré un week-end plus copieux.

---

## 7. Synthèse des tendances et variations notables (S25 → S26)

| Indicateur | S25 | S26 | Variation | Cohérence plan |
|-----------|-----|-----|-----------|----------------|
| **Poids moyen (calculé)** | 75.62 kg | 75.43 kg | -0.20 kg | ✓ cohérent palier Phase 4 |
| **Sommeil moyen (sleeping_history)** | 7h11 | 7h41 | +30 min | ✓ objectif >7h10 atteint |
| **Coucher moyen** | 11:43 PM | 11:48 PM | +5 min | ⚠ pas d’avance nette |
| **Lever moyen** | 6:57 AM | 7:34 AM | +37 min | ✓ contribue au gain |
| **Activités complétées** | 2/3 | 3/3 | +1 séance | ✓ mais tempo un peu trop haut |
| **Signal lombaire** | niveau 2 week-end | niveau 2 samedi soir | = (profil différent) | ⚠ reste point de vigilance |
| **Signal genou** | RAS (rapporté) | léger en EF | ↑ (léger) | ⚠ à surveiller |

---

## 8. Biais et limitations

### Limitations données quantifiées
1. **Poids S26** : 4 mesures sur 7 jours (manque 02/02, 04/02, 08/02). La moyenne est donc indicative.
2. **Sommeil** : données complètes 7/7 (bonne fiabilité). Néanmoins, l’amélioration moyenne est influencée par une nuit très longue (10h29).
3. **Charge running** : absence d’infos type dénivelé, surface, cadence. FC et allure partiellement renseignées, mais la charge mécanique lombaire reste partiellement non observée.

### Biais potentiels
- **Attribution causale lombaire** : en S26, le lien avec la séance tempo est plausible (signal en séance + RPE/FC élevés), mais ce n’est pas une preuve.
- **Heure de coucher vs durée** : la durée moyenne augmente malgré des couchers parfois tardifs (1:17 AM). L’amélioration peut venir d’un rythme de lever plus tardif plutôt que d’une hygiène “coucher tôt”.
 - **Week-end** : une partie des résultats sommeil (durées longues + couchers tardifs) est influencée par l’absence de contrainte de réveil, donc transférabilité en semaine contrainte à vérifier.

### Exhaustivité données (règle CIH Étape 1)
- ✓ weight_history.csv : consulté (comparaison S25→S26 quantifiée)
- ✓ sleeping_history.csv : consulté (comparaison S25→S26 quantifiée)
- ✓ Sommeil.csv S26 : exploité intégralement
- ✓ plan_semaine_26.md et bilan_semaine_26.md : consultés intégralement

---

## 9. Conclusions analytiques (sans prescription)

1. **Sommeil** : amélioration nette (+30 min), objectif S26 atteint ; gain porté par des levers plus tardifs et une nuit de récupération très longue, dans un contexte week-end sans contrainte de réveil.
2. **Poids** : légère baisse (-0.2 kg estimée) ; trajectoire compatible avec fin Phase 4 et palier ~75–75.5.
3. **Activités** : conformité 3/3 ; la séance tempo apparaît comme le principal facteur de risque mécanique (RPE au-dessus cible, signal lombaire en séance).
4. **Lombaire** : profil plus “événementiel” (tempo) que S25 (plus diffus). Le pic en séance est confirmé à 2/4 avec retour à 0 le lendemain matin.
5. **Genou** : signal léger isolé sur EF ; à surveiller mais pas d’escalade rapportée.

---

## 10. Intégration du feedback utilisateur (Clarifications Étape 1)

### Réponses utilisateur intégrées

**Q1 — Lombaire séance tempo (samedi)** : pic confirmé à **2/4 pendant la séance** ; **retour à 0/4 le lendemain matin**. → Renforce l’interprétation d’un signal **transitoire** associé à la séance qualité (sans persistance lendemain).

**Q2 — Nuit très longue du 07/02 (10h29)** : contexte **week-end sans contrainte de réveil**, avec **probable récupération**, sans ressenti marqué de dette de sommeil sur la semaine. → Indique que l’amélioration moyenne S26 est en partie portée par l’opportunité week-end, pas nécessairement par une avance du coucher.

**Q3 — Couchers tardifs (07/02, 08/02)** : **totalement choisis**, week-end, sans contrainte de réveil. → Confirme que l’hygiène “coucher tôt” n’est pas le levier principal de cette semaine ; la durée de sommeil est néanmoins élevée.

### Synthèse après clarifications
Les réponses utilisateur **ne changent pas les constats chiffrés** (sommeil en hausse, poids stable/baisse légère, 3/3 activités) mais précisent que :
- le signal lombaire tempo est **réel mais non persistant** (pic 2/4, retour 0/4 lendemain),
- le gain de sommeil est **fortement influencé par le week-end** (levers tardifs + couchers tardifs choisis).
