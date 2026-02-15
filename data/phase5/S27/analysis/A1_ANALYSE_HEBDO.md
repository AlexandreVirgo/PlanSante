# A1_ANALYSE_HEBDO — Semaine 27

## Métadonnées
- **Semaine analysée** : S27
- **Période couverte** : 9 février 2026 – 15 février 2026
- **Phase active** : Phase 5 (stabilisation structurée)
- **Rôle exécuteur** : PS-ANA-02 (Analyse factuelle)
- **Date génération** : 15 février 2026
- **Artefacts sources** : bilan_semaine_27.md, plan_semaine_27.md, weight_history.csv, sleeping_history.csv, Sommeil.csv (S27), R_HEBDO_S26.md

---

## 1. Analyse pondérale

### Données brutes S27 (weight_history.csv)
- 2026-02-09 : 77.0 kg
- 2026-02-10 : 76.1 kg
- 2026-02-11 : 76.1 kg
- 2026-02-12 : 75.4 kg
- 2026-02-14 : 76.2 kg

**Poids moyen S27 (calculé sur points disponibles)** : **76.16 kg** (n=5)

### Comparaison temporelle S26 → S27
- **Poids moyen S26 (calculé)** : **75.43 kg** (n=4, 03/02 au 07/02)
- **Poids moyen S27 (calculé)** : **76.16 kg** (n=5, 09/02 au 14/02)
- **Variation S26→S27** : **+0.73 kg**

**Notes factuelles** :
- Le bilan S27 indique **poids moyen 76.2 kg**, cohérent avec la moyenne calculée.
- La hausse vs S26 est compatible avec une transition **Phase 4 (diète)** → **Phase 5 (stabilisation)** + bruit hydrique/glycogène (et un repas copieux type raclette signalé le samedi).

---

## 2. Analyse sommeil

### Données consolidées S27 (sleeping_history.csv)
- **Sommeil moyen S27** : **7h 38m**
- **Heure de coucher moyenne S27** : **11:56 PM**
- **Heure de lever moyenne S27** : **7:40 AM**

### Comparaison temporelle S26 → S27 (sleeping_history.csv)
- **Sommeil moyen S26** : 7h 41m → **S27** : 7h 38m (**-3 min**)
- **Coucher moyen S26** : 11:48 PM → **S27** : 11:56 PM (**+8 min**, plus tard)
- **Lever moyen S26** : 7:34 AM → **S27** : 7:40 AM (**+6 min**, plus tard)

**Observation clé** : la durée reste élevée (~7h38) mais l’objectif Phase 5 de coucher **22h30/23h** n’est pas atteint en moyenne (coucher consolidé ~23h56).

### Données quotidiennes S27 (Sommeil.csv)
| Date | Durée | Coucher | Lever |
|------|-------|---------|-------|
| 2026-02-09 | 6h 38m | 11:42 PM | 6:21 AM |
| 2026-02-10 | 7h 50m | 11:11 PM | 7:03 AM |
| 2026-02-11 | 6h 23m | 12:05 AM | 6:31 AM |
| 2026-02-12 | 9h 35m | 11:14 PM | 8:58 AM |
| 2026-02-13 | 8h 31m | 11:06 PM | 7:52 AM |
| 2026-02-14 | 7h 07m | 1:00 AM | 8:17 AM |
| 2026-02-15 | 7h 27m | 1:14 AM | 8:43 AM |

**Durée moyenne calculée (7 jours)** : **7h 38m** (cohérent sleeping_history.csv)

**Notes factuelles** :
- 2 nuits < 7h : 6h38 (09/02) et 6h23 (11/02)
- 2 couchers très tardifs (week-end) : 01:00 (14/02) et 01:14 (15/02)
- 0 nuit avec coucher ≤ 23:00 (selon Sommeil.csv)

---

## 3. Analyse activités physiques

### Conformité plan S27
Plan S27 : 3 séances (FB + EF + Fartlek), avec **1 seule séance qualité** strictement contrôlée.

| Activité planifiée | Statut | Notes factuelles |
|-------------------|--------|------------------|
| FB-30-BASE-V1 (Lun/Mar, RPE 5–6) | ✓ Complétée | Lundi midi. RPE 5. FC moy 117, max 155. Pont fessier +2 séries. Aucun signal lombaire/genou. |
| RUN-40-EF-V1 (Jeudi, RPE 2–3) | ✓ Complétée | Jeudi midi. RPE 4–5 (ressenti facile mais FC haute). FC moy 158, max 174. 40 min, 8:22/km. ~50% zone 3 / 50% zone 4. Aucun signal genou. Raideur lombaire légère fin de séance sans douleur. |
| RUN-40-FARTLEK-V1 (Samedi, RPE base 2–3 / acc 6) | ✓ Complétée | Samedi. Parcours vallonné, accélérations montée/descente. RPE 6–7 sur accélérations. FC moy 156, max 180 (données partielles : montre arrêtée sur dernier tiers). Aucun signal lombaire/genou. |

### Activité non prévue
| Activité | Statut | Notes factuelles |
|---------|--------|------------------|
| RUN-50-EF-V1 (Dimanche) | ✓ Ajoutée | Dimanche. 50 min, 9:09/km. RPE 3. FC moy 145, max 165. 75% zone 3 / 25% zone 2. Aucun signal lombaire/genou. |

**Conformité globale** : 3/3 séances planifiées réalisées + **1 séance supplémentaire** (volume hebdo ↑). Les données FC indiquent une intensité cardiovasculaire plus élevée que la cible sur les séances EF (jeudi + dimanche), malgré un RPE bas à modéré.

---

## 4. Analyse signaux corporels

### Lombaire
- S27 : **RAS** (bilan) avec **raideur légère** en fin de séance EF jeudi (sans douleur) ; aucun signal reporté sur fartlek ni sur l’EF dimanche.

### Genou
- S27 : **aucun signal** reporté (y compris EF)

### Énergie / motivation / humeur / digestion
- **Énergie** : bonne
- **Motivation** : bonne
- **Humeur** : positive
- **Digestion** : RAS
- **Sommeil (qualitatif)** : “correct” (bilan)

---

## 5. Analyse nutrition — Phase 5

### Adhérence rapportée
- Consignes : respectées
- Semaine : repas alignés recommandations
- Samedi : raclette + dessert (repas plus copieux)
- Chocolat : consommation plus faible mais **non quantifiée**
- Alcool : consommation plus faible, selon recommandations

---

## 6. Synthèse des tendances et variations notables (S26 → S27)

| Indicateur | S26 | S27 | Variation | Lecture factuelle |
|-----------|-----|-----|-----------|------------------|
| **Poids moyen (calculé)** | 75.43 kg | 76.16 kg | +0.73 kg | hausse compatible transition diète→stabilisation + variabilité | 
| **Sommeil moyen (consolidé)** | 7h41 | 7h38 | -3 min | stable élevé | 
| **Coucher moyen** | 11:48 PM | 11:56 PM | +8 min | un peu plus tard | 
| **Activités** | 3/3 | 3/3 + 1 ajout | volume ↑ | adhérence + surcharge potentielle | 
| **Lombaire** | signal modéré événementiel (tempo) | RAS (raideur légère EF) | amélioration | garde-fous semble efficace | 
| **Genou** | léger signal isolé | RAS | amélioration | à confirmer sur durée | 

---

## 7. Biais et limitations

1. **Poids S27** : 5 mesures sur 7 jours (manque 13/02, 15/02). La moyenne reste indicative.
2. **Attribution causale poids** : l’écart S26→S27 peut refléter une partie “retour glycogène/eau” + repas copieux ; non distinguable d’un gain réel sans série plus dense.
3. **FC / zones cardio** : zones potentiellement approximatives (calibration montre) ; et données **partielles** sur fartlek (arrêt montre dernier tiers).
4. **Sommeil vs objectif Phase 5** : la durée est bonne mais l’objectif de coucher 22h30/23h n’est pas atteint sur la semaine (Sommeil.csv).
5. **Nutrition** : chocolat/alcool mentionnés mais non quantifiés → pas de comparaison chiffrée possible.

### Clarification utilisateur (zones FC)
- Les zones FC utilisées par la montre sont basées sur des **% de FC max**, avec une **FC max estimée** sur des observations (~1 an, boxe), sans test spécifique FC max / seuil.
- Conséquence possible : si la FC max de référence est sous-estimée, la montre peut classer une partie de l’effort en zones “hautes” alors que l’effort est réellement plus modéré (ou inversement).

### Exhaustivité données (règle CIH Étape 1)
- ✓ weight_history.csv : consulté (comparaison S26→S27 quantifiée)
- ✓ sleeping_history.csv : consulté (comparaison S26→S27 quantifiée)
- ✓ Sommeil.csv S27 : exploité intégralement
- ✓ plan_semaine_27.md et bilan_semaine_27.md : consultés intégralement
- ✓ R_HEBDO_S26.md : consulté

---

## 8. Conclusions analytiques (sans prescription)

1. **Poids** : moyenne S27 ~76.16 kg, soit +0.73 kg vs S26 ; hausse plausible et attendue en contexte de transition vers stabilisation, avec variabilité liée au week-end.
2. **Sommeil** : durée stable élevée (~7h38) mais les heures de coucher restent tardives ; l’objectif de “coucher 22h30/23h la majorité des nuits” n’est pas atteint sur la base des données S27.
3. **Charge / intensité** : 3 séances prévues réalisées + 1 sortie ajoutée ; FC élevée sur EF (jeudi) malgré RPE modéré, suggérant dérive d’intensité cardio (ou zones trop strictes / mesure).
4. **Signaux corporels** : lombaire globalement RAS (raideur légère isolée) et genou RAS ; profil nettement plus favorable que S26 sur la dimension lombaire.

---

## 9. Intégration du feedback utilisateur (Clarifications Étape 1)

### Réponses utilisateur intégrées

**Q1 — Couchers tardifs (S27)** : confirmés comme **choisis** (plutôt que subis). → Oriente la lecture vers un levier “routine/choix” plutôt qu’un trouble de sommeil non contrôlable.

**Q2 — Zones FC** : zones basées sur **% FC max**, FC max **estimée** (observations lors de la boxe, ~1 an) sans test formel. → Renforce la limitation “calibration zones” et explique qu’une FC “haute en zones” peut refléter en partie un paramétrage plutôt qu’une intensité réellement trop élevée.

**Q3 — Pic de poids (09/02 à 77.0 kg)** : contexte week-end familial (repas plus riches) ; pesée dans des conditions standard (matin à jeun après selle). → Rend l’explication “variabilité hydrique/stockage” plausible sans remettre en cause la comparabilité des mesures.

### Synthèse après clarifications
Les réponses utilisateur ne changent pas les constats chiffrés (poids moyen S27 ~76.16, sommeil ~7h38, 3/3 + 1 séance) mais précisent que :
- le coucher tardif est principalement **comportemental** (choisi),
- l’interprétation des zones FC doit être **prudente** sans calibration récente/robuste,
- le pic de poids du 09/02 est cohérent avec un contexte week-end, avec mesure comparable.
