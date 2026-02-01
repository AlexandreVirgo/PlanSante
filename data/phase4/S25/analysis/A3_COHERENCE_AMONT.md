# A3_COHERENCE_AMONT — Semaine 25

## Métadonnées
- **Semaine analysée** : S25
- **Période couverte** : 26 janvier – 1 février 2026
- **Rôle exécuteur** : PS-COH-04 (Contrôle de cohérence amont)
- **Date génération** : 1 février 2026
- **Artefacts sources** : A1_ANALYSE_HEBDO.md, A2_SIGNAUX_FAIBLES.md, plan_semaine_25.md, project_registry.md, phase4.md

---

## 1. Cadre de cohérence

**Objectif** : Identifier incohérences potentielles entre :
- **Exécution S25** (faits observés, signaux)
- **Plan S25** (prévisions, objectifs)
- **Registry projet** (contraintes non-négociables, hypothèses, indicateurs)
- **Phase 4** (objectifs, règles, critères réussite)

**Codification tensions** :
- 🔴 **Critique** : Violation directe contrainte non-négociable OU précurseur d'escalade vers violation
- 🟡 **Mineure** : Déviation observable, impactant moyen ou long-terme, non-violation directe
- 🟢 **Conforme** : Exécution cohérente avec plan/registry/phase

**Aucun jugement d'opportunité** : rôle PS-COH-04 = détection logique, pas arbitrage.

---

## 2. Cohérences validées

### 🟢 Conformité activités adaptatif gérée

**Assertion** : Plan S25 prévoyait 3 activités (FB-30, RUN-40-EF, RUN-40-TEMPO). Exécution : 2/3 (omission tempo).

**Vérification** :
- Plan S25, § Activités : « Adapter immédiatement en cas de signal lombaire ou articulaire »
- Bilan S25 : signal lombaire niveau 2 (persistant sam–dim) observé
- Décision exécution : utilisateur a omis séance tempo en réaction au signal
- Registry projet, § Contraintes : « Priorité à la santé : aucune stratégie ne doit dégrader [...] la santé lombaire »

**Cohérence** : ✓ **VALIDE**. Omission activité justifiée par signal corporel, conforme directive plan S25 et contrainte projet (santé lombaire prioritaire). Aucune incohérence logique.

---

### 🟢 Nutrition Phase 4 cadre respecté

**Assertion** : Bilan rapporte « consignes respectées ». Plan S25 prévoyait Phase 4 strict (féculents 80–120g/j selon jour).

**Vérification** :
- Bilan S25 : « Pas de difficultés majeures, [...] Toujours une consommation carreaux chocolat noir le soir »
- Écarts mineurs documentés (chocolat quotidien vs 2–3×/sem, alcool weekend) mais acceptables volumétriquement
- Phase 4 critères réussite : « aucun besoin de durcir les règles pour obtenir des résultats »
- Poids observé : -0.2 kg (compatible décrue Phase 4 modérée)

**Cohérence** : ✓ **VALIDE**. Cadre Phase 4 respecté ; écarts mineurs acceptables et documentés. Perte pondérale compatible (palier normal, non anomalie).

---

### 🟢 Timing coucher optimisé vs plan hygiène sommeil

**Assertion** : Plan S25 prioritaire = « Hygiène sommeil prioritaire : Coucher vers 23h00–23h30 ». Exécution : coucher moyen 11:42 PM (avancé 23 min vs S24).

**Vérification** :
- Plan S25 objectif : « > 7h minimum hygiène sommeil »
- Exécution S25 : timing coucher conforme (11:42 PM = ~23:42, quasi-centre cible 23h–23h30)
- Avance vs S24 = amélioration relative

**Cohérence** : ✓ **VALIDE**. Timing coucher optimisé, conforme plan priorité hygiène sommeil.

---

### 🟢 Genou monitoring et réduction charge effective

**Assertion** : Plan S25 = RUN-40-EF (réduction vs S24 RUN-45-EF) avec instruction monitoring. Exécution : 0 signal génou S25 (vs léger S24).

**Vérification** :
- Plan S25, RUN-40-EF : « Réduction charge : RUN-40-EF (vs RUN-45-EF S24) »
- Phase 4 règle : « Adaptation immédiate en cas de signal [...] articulaire »
- Résultat : aucun signal genou S25
- Indicateur registry : « Maintien ou amélioration des capacités sportives à charge équivalente »

**Cohérence** : ✓ **VALIDE**. Ajustement charge justifié et efficace ; genou capacité adaptive confirmée.

---

## 3. Incohérences potentielles détectées

### 🔴 CRITIQUE — Signal lombaire escalade : violation risquée de contrainte « santé lombaire »

**Assertion** : Bilan S25 rapporte douleur lombaire niveau 2 (modérée) persistant sam–dim. Registry projet § Contraintes : « Priorité à la santé : aucune stratégie ne doit dégrader [...] la santé lombaire ».

**Détail incohérence** :
1. **Fait observé** : Signal lombaire S25 **escalade vs S24**
   - S24 : léger (0–1), ergonomique (bureau), résolvable repositionnement
   - S25 : modéré (2), tardif (sam–dim), persistant, mécanique/postural (douleur respiration, mouvements, marche, posture droite)
   
2. **Profil signal** : Mécanique/postural clair, déclencheurs identifiés (respiration profonde, mouvements, marche, posture droite). Profil **différent** de fatigue simple = possible dysfonction posturo-motrice ou inflammation/contraction.

3. **Causalité implicite dans Phase 4** : Phase 4 § Critères réussite : « Absence de douleur lombaire persistante ». S25 présente douleur persistante (2 jours consécutifs niveau 2).

4. **Contrainte registry non-violée techniquement (encore)** : Utilisateur a omis séance 3 (tempo) pour éviter escalade. Mais escalade **déjà observée au moment de la décision** (sam–dim niveau 2). Omission = action correctrice, pas prévention.

5. **Risque escalade S26** : Pattern signal lombaire tardif (sam–dim) sur 2 jours = point de vigilance. Si récurrence S26 même intensité ou ampleur → **signal d'escalade confirmé** → nécessité révision Phase 4 (prolongement, modulation, ou exit).

**Incohérence logique** :
- Phase 4 cadre suppose **absence escalade douleur lombaire**
- S25 observe **escalade douleur lombaire**
- Phase 4 continuation (Option 0 S24 = continuity S25–S26) suppose escalade N'aura PAS lieu
- Escalade observée S25 = **contradiction latente entre hypothèse Phase 4 et observation empirique**

**Gravité** : 🔴 **CRITIQUE** — Violation implicite contrainte santé lombaire ; mais limitée S25 par action adaptative (omission activité). Risque escalade S26 = **point d'arbitrage décisionnel clé**.

**Recommandation triage** : Nécessité monitoring strict S26 pour confirmer/infirmer pattern. Si confirmé S26 = exit Phase 4 anticipée ou modulation.

---

### 🔴 CRITIQUE — Objectif sommeil S25 raté de 2 minutes : impact sur fatigue tardive

**Assertion** : Plan S25 objectif sommeil : « > 7h10 min ». Exécution S25 : 7h 8m moyen.

**Détail incohérence** :
1. **Fait observé** : Sommeil 7h 8m vs objectif > 7h10m = 2 min sous-cible
2. **Contexte cause** : Nuit 31 jan très courte (5h50, coucher tard 1:19 AM + réveil intempestif) = volatilité causale identifiée
3. **Hypothèse sleep-quality → fatigue lombaire** : Registry projet § Hypothèses : « Les signaux corporels [...] priment sur données chiffrées ». Qualité sommeil (volatilité + nuit courte) probable contributrice à fatigue neuromusculaire tardive → escalade lombaire
4. **Plan S25 prévention** : « Hygiène sommeil prioritaire » censée prévenir récurrence S24 (baisse -32 min). S25 +2 min vs S24, mais sous-objectif 7h10.

**Incohérence logique** :
- Objectif plan = 7h10+ pour récupération vs S24 basse (baisse -32 min)
- Exécution = 7h8m (quasi-égal S24 7h6m) = **récupération not achieved**
- Sommeil insuffisant impliqué dans fatigue lombaire escalade (selon hypothèses cumulatives)
- Donc : Plan hygiène sommeil **objectif raté** → implicite récupération insuffisante → implicite fatigue lombaire escalade

**Gravité** : 🔴 **CRITIQUE** — Objectif sommeil raté impacte récupération neuromusculaire → corrélé escalade lombaire. Nuit 31 jan (événement social) = cause secondaire acceptable, mais sommeil volatilité intra-semaine (pattern observable) = point vulnérabilité Phase 4.

**Recommandation triage** : S26 priorité absolue = sommeil > 7h10 solidifié (nuit courte 31 jan isolée ou pattern établi ?). Si pattern s'établit (volatilité récurrente) → Phase 4 devient **incompatible** avec contrainte récupération.

---

### 🟡 MINEUR — Séance EF 1h vs 40 min : surcharge implicite, compensation adaptative validée

**Assertion** : Plan S25 = RUN-40-EF (40 min prévu). Exécution = RUN-40-EF (1h réalisé, itinéraire mal calibré).

**Détail incohérence** :
1. **Fait observé** : Séance EF 25 min plus longue que prévue (1h vs 40 min)
2. **Compensation** : Utilisateur a intentionnellement réduit intensité (alternance marche/course lente) → charge métabolique probable < durée apparente
3. **Impact** : Hypothèse cumul fatigue neuromusculaire (2 séances S25) = contributif à lombaire escalade. Séance 1h (même si intensité réduite) = cumul volume vs rythme habituel.

**Incohérence logique** :
- Plan = 40 min RUN-40-EF (charge modérée)
- Exécution = 1h RUN-40-EF (durée +50%, mais intensité réduite compensatoire)
- Cumul avec FB-30 rapprochée (2 séances dans semaine, sans séance qualité tempo) = charge cumulative possible vecteur fatigue
- Phase 4 règle : « Aucune augmentation simultanée marquée de charge sportive et déficit énergétique »
- S25 observé : charge légère augmentation (séance 1h) + déficit énergétique Phase 4 (continu) = **possible violation implicite règle Phase 4**

**Gravité** : 🟡 **MINEUR** — Compensation adaptative utilisateur (réduction intensité) valide techniquement. Mais cumul volume (2 séances rapprochées + séance EF prolongée) = facteur contributif observable à fatigue tardive/escalade lombaire. Pas violation stricte Phase 4 (intensité compensée), mais pattern à monitorer S26.

**Recommandation triage** : S26 = confirmer capacité récupération après semaine cumul volume. Si signal lombaire récurrence → ajuster planning activités (espacer davantage, ou réduire durée absolue).

---

### 🟡 MINEUR — Écart chocolat quotidien : acceptable mais observable

**Assertion** : Plan = chocolat 2–3×/sem (20–30g). Exécution = quotidien (estimé 20–30g/j = 7×/sem).

**Vérification** :
- Plan S25 : « Sucré intentionnel et limité (ex. 20–30g chocolat noir, 2–3×/sem) »
- Bilan S25 : « Toujours une consommation carreaux chocolat noir le soir »
- Surplus : ~70–150 kcal/sem compatible perte 0.2 kg observé

**Incohérence logique** :
- Plan explicit : 2–3×/sem
- Exécution observed : 7/7 j
- Registry projet § Durabilité : « Absence de restrictions extrêmes ou de comportements compensatoires »

**Analyse** : Pattern chocolat quotidien = consommation stable S25 (non escalade), volontaire et assumée par utilisateur. Surplus calorique marginal (compatible résultats). Mais déviation observable vs plan.

**Gravité** : 🟡 **MINEUR** — Déviation documentée, volumétriquement acceptable. Non-escalade pattern. Acceptable court-terme sous assumption durabilité ("comportement assumé = plus durable que privation"). À monitorer si escalade quantité.

**Recommandation triage** : Accepter comme pattern stable ; noter pour feedback S26 (justifier si applicable, ou réaligner plan S26 pour chocolat quotidien vs 2–3×/sem).

---

## 4. Synthèse tensions structurantes

| Tension | Gravité | Nature logique | Impact immédiat | Risque escalade |
|---------|---------|-----------------|-----------------|-----------------|
| **Escalade lombaire** | 🔴 Critique | Fait observable (escalade) vs Phase 4 hypothèse (absence escalade) | Utilisateur a adapté (omis séance) ; escalade observée quand même | **S26 monitoring strict** = key decision point |
| **Sommeil sous-objectif** | 🔴 Critique | Objectif raté (7h8 vs 7h10+) vs plan priorité sommeil | Volatilité intra-semaine + nuit courte = fatigue tardive probable | **S26 solidification sommeil** = prerequisite continuation Phase 4 |
| **Surcharge EF implicite** | 🟡 Mineure | Cumul volume (séance 1h + 2 séances rapprochées) vs Phase 4 règle « pas augmentation simultanée » | Pattern observable mais compensé intensité ; contributif possible à fatigue | S26 : monitor récupération post-cumul |
| **Écart chocolat** | 🟡 Mineure | Déviation plan (quotidien vs 2–3×/sem) vs exécution | Marginal volumétriquement ; stable, assumé | Faible si pattern stable ; accepter ou réaligner S26 |

---

## 5. Validations de cohérence réussies (positives)

- ✓ Activités adaptivement gérées (omission justifiée par signal)
- ✓ Nutrition Phase 4 cadre respecté, décrue conforme
- ✓ Timing coucher optimisé vs plan hygiène
- ✓ Genou monitoring effectif, ajustement charge productive
- ✓ Stress professionnel baissé (conforme plan S25 expectation)
- ✓ Énergie améliorée (cohérent avec récupération sommeil relative)
- ✓ Motivation et humeur stables (compatibles Phase 4)
- ✓ Digestion RAS (tolérance nutritionnelle confirmée)

---

## 6. Points de vigilance prioritaires pour Étape suivante

### **Majeur : Escalade lombaire + sous-objectif sommeil (dans contexte Phase 4 3/4)**
Ces 2 signaux critiques **contradisent hypothèse Phase 4 continuation sans modification**. Contexte clé : S25 = semaine 3/4 Phase 4 (dernière semaine = S26). Utilisateur accepte continuer test S26 et accepterait modulation si escalade persistante S26. **S26 = test décisif final** : récurrence lombalgie ET sommeil < 7h10 → exit Phase 4 accélérée (plutôt que prolongation) = compatible avec transition stabilisation de toute façon.

### **Mineur : Pattern cumul volume activités**
Séance EF 1h + 2 séances rapprochées (sans tempo qualité) = cumul probable contributif. S26 espacer davantage, ou réduire durée absolue, ou prévoir séance qualité plus tôt (vs fin semaine).

### **Minor : Volatilité sommeil intra-semaine (nuit 31 jan isolée)**
Nuit 31 jan cause (social, réveil intempestif) identifiée. Utilisateur confirme événement social **isolé** (pas pattern attendu S26). S26 monitoring : nuit courte ne doit pas se reproduire.

---

## 7. Contexte décisionnel clé (S25 = semaine 3/4 Phase 4)

**Clarification utilisateur intégrée** : S25 est **déjà la semaine 3/4 de Phase 4**. Implication stratégique majeure :
- S26 = **dernière semaine Phase 4** (semaine 4/4)
- S26 soir = point de décision forcée : **exit Phase 4 et transition vers phase de stabilisation**, ou prolongement au-delà de 4 semaines

**Impact sur risque escalade lombaire** : 
- Incohérences critiques S25 (escalade lombaire + sommeil insuffisant) ne sont **pas** problèmes court-terme isolation S25 (vous acceptez continuer test S26)
- But **S26 devient test décisif** : escalade lombaire récurrence S26 = signal direct pour exit Phase 4 (plutôt que prolongation indefinite)
- Phase 4 sortie S26 soir était **prévue** dans registry projet ("S26 soir : Évaluation formelle [...] avant décision passage **phase de stabilisation structurée**")

**Reclassification risques** : Escalade lombaire S25 + sommeil insuffisant = **points de monitoring S26**, pas blocages immédiats. Mais **S26 décision irrévocable** : pas de semaine 5 Phase 4 attendue. Donc incohérences critiques S25 = input direct pour options S26 (modifier semaine 4, ou exit accélérée).

---

## 8. Aucun jugement d'opportunité

Rôle PS-COH-04 : **détection logique uniquement**. Pas d'arbitrage, pas de recommandation stratégique.

Incohérences identifiées = **input pour Étape 4 (PS-STR-01 structuration)** et **Étape 5 (PS-DIR-07 options stratégiques)**.
