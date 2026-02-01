# A2_SIGNAUX_FAIBLES — Semaine 25

## Métadonnées
- **Semaine analysée** : S25
- **Période couverte** : 26 janvier – 1 février 2026
- **Rôle exécuteur** : PS-SIG-05 (Détection de signaux faibles)
- **Date génération** : 1 février 2026
- **Artefact source** : A1_ANALYSE_HEBDO.md
- **Données utilisateur brutes** : bilan_semaine_25.md, clarifications utilisateur post-A1

---

## 1. Cadre de détection

**Signaux détectés** : anomalies, variations anormales, dégradations, améliorations inhabituelles, écarts par rapport au plan ou à la baseline historique.

**Codification gravité** :
- 🔴 **Majeur** : impactant directement santé, performance, ou adhérence plan ; risque escalade court-terme
- 🟡 **Mineur** : déviation acceptable mais observable ; impactant indirectement ou long-terme
- 🟢 **Positif** : amélioration observable vs baseline ou attentes plan

**Certitude** : niveau d'incertitude sur étiologie (non diagnostic, pas d'attribution causale exclusive)

---

## 2. Signaux détectés S25

### 🔴 MAJEUR — Signal lombaire : escalade et persistance

| Attribut | Valeur |
|----------|--------|
| **Description** | Douleur lombaire niveau 2 (modérée, échelle 0–4) persistante samedi–dimanche (2 jours consécutifs) |
| **Profil temporel** | Lun–Ven : signaux légers (0–1) et transitoires. Sam–Dim : escalade à 2, persistant |
| **Contexte occurrence** | Fin de semaine, 2–3 jours après dernière activité physique. Aucun signal rapporté **pendant** exécution séances |
| **Profil douleur** | **Mécanique/postural** : localisée zone lombaire/bassin. Déclencheurs : respiration profonde diaphragmatique, mouvements, marche, posture droite. Profil différent de « fatigue musculaire » — suggère dysfonction posturo-motrice ou rigidité/blocage mécanique |
| **Impact psycho-émotionnel** | Fatigue légère samedi (attendue post-nuit courte). **Impact principal : moral et irritabilité** → facteur nerveux/émotionnel possible en plus de mécanique |
| **Novité vs S24** | **OUI, changement de profil** : S24 signaux ergonomiques (bureau), legers (0–1), résolvables repositionnement. S25 signaux tardifs, plus intenses, **mécanique/postural** (vs ergonomique), non-expliqués immédiatement |
| **Facteurs concomitants** | Cumul fatigue neuromusculaire (2 séances S25 rapprochées), volatilité sommeil (notamment nuit 31 jan : 5h50, coucher tard assumé + réveil naturel intempestif + mauvaise récupération montre), déficit énergétique Phase 4 cumulatif, facteur nerveux/stress local |
| **Hypothèses étiologiques** | (1) Dysfonction posturo-motrice post-cumul 2 séances (stabilisateurs lombaires fatigués, compensation posturale) ; (2) Rigidité/blocage mécanique (inflammatoire ou contracturé) post-effort ; (3) Récupération neuromusculaire défaillante (sommeil volatile S25, impact nuit 31 jan) ; (4) Interaction Phase 4 + charge motrice + récupération ; (5) Facteur émotionnel/nerveux amplificateur (irritabilité rapportée) ; (6) Facteur externe non-identifié (posture assise prolongée, micro-traumatisme) |
| **Certitude étiologie** | **Moyenne** : profil mécanique/postural clair (déclencheurs précis identifiables). Étiologie reste multifactorielle probable, aucune exclusive falsifiable. Impact psycho-émotionnel (irritabilité) ajoute complexité. |
| **Risque escalade court-terme** | **Modéré** : persistance de pattern « tardif » sur Sam–Dim requiert monitoring. Si récurrence S26 à intensité égale ou supérieure → signal d'escalade confirmé → nécessité ajustement Phase 4 ou repos différencié |
| **Indicateur de santé menacé** | OUI : constraint non-négociable « santé lombaire » ([project_registry.md](/project_registry.md)) |

**Détail quotidien S25** :
- Lun 1/27 : 0 (baseline)
- Mar 1/28 : 1 → 0 (transitoire, post-FB-30)
- Mer 1/29 : 0 (baseline, post-RUN-EF)
- Jeu 1/30 : 1 → 0 (transitoire)
- Ven 1/31 : 1 → 0 (transitoire)
- **Sam 2/1 : 2 (persistant)**
- **Dim 2/2 : 2 (persistant)**

**Action déjà prise** : Omission volontaire séance 3 (tempo) en réaction au signal = adaptabilité confirme, approche conservatrice respectée.

---

### 🟡 MINEUR — Volatilité sommeil S25

| Attribut | Valeur |
|----------|--------|
| **Description** | Variation importante durée sommeil intra-semaine (5h50 min – 7h56 min = écart 2h6m) |
| **Profil temporel** | Nuit isolée très courte (31 jan : 5h50), entourée de nuits correctes (7h13–7h56). Moyenne semaine 7h8m (quasi-stable vs S24 7h6m) |
| **Novité vs S24** | NON, volatilité présente S24 aussi. S25 : volatilité **identique ordre de grandeur** (~1h variation courante) |
| **Causes identifiées** | Nuit 31 jan : choix social (coucher tard 1:19 AM, intention dormir samedi AM) + réveil naturel intempestif samedi AM + données montre « récupération relativement mauvaise ». Autres nuits : régularité acceptable, timing coucher optimisé vs S24 (-23 min avancé) |
| **Impactants** | Probable contribution à fatigue neuromusculaire tardive (cumul avec 2 séances) ; corrélation objective avec escalade signal lombaire (hypothèse : récupération neuromusculaire entravée) |
| **Certitude** | **Moyenne** : cause identifiée (nuit 31) ; autres nuits conformes plan. Corrélation sleepquality–lombaire plausible mais non-causalité exclusive |
| **Risque escalade** | **Faible si nuit 31 isolée** ; **modéré si pattern s'établit** (couchers tardifs récurrents) |

**Indicateur de santé menacé** : OUI : constraint « priorité sommeil » ([project_registry.md](/project_registry.md), S25 plan)

---

### 🟡 MINEUR — Écarts nutrition mineurs (multiples)

#### Écart 1 : Chocolat quotidien vs 2–3×/semaine prévue

| Attribut | Valeur |
|----------|--------|
| **Description** | Chocolat noir consommé 7/7 jours (quotidien) vs plan 2–3×/sem |
| **Quantification** | Plan : 20–30g, 2–3×/sem = 40–90g/sem. Observé : estimé ~20–30g/jour × 7 = 140–210g/sem. Surplus : +50–120g/sem |
| **Impactant calorique** | Surplus estimé 70–150 kcal/sem = compatible perte 0.2 kg observé (légère) |
| **Novité** | Pattern stable S25 rapporté « toujours une consommation carreaux chocolat noir le soir » (habitude établie, non escalade) |
| **Certitude** | **Haute** : consommation observée quotidienne, documentée bilan |
| **Risque escalade** | **Faible** : flux stable, pas augmentation progressive ; cohérent avec « durabilité » projet |

#### Écart 2 : Alcool weekend élevé

| Attribut | Valeur |
|----------|--------|
| **Description** | Alcool weekend vin + apéritif anisé vs plan 0 semaine, tolérance ponctuelle weekend |
| **Quantification** | Type : vin (modéré) + anisé (modéré-doux). Quantité : « ~5 verres/jour » fin de semaine = estimation utilisateur, profil modéré (non alcools forts). Implicite : 2 jours × 5 = ~10 verres fin de semaine vs plan ~0–2 verres tolérés |
| **Impactant** | Hydratation (poids), récupération sommeil (si alcool + sommeil court = compounded), digestion (rapporté RAS) |
| **Novité** | Consignation début semaine « alcool weekend supérieur à la recommandation » = utilisateur conscient déviation |
| **Certitude** | **Moyenne** : quantification modérée (vin/anisé, pas alcools forts), but reconnaissable (weekend social) |
| **Risque escalade** | **Faible-modéré** : événement social assumé ; profil modéré (vs alcools forts) = impactant hydratation/récupération limité |

**Bilan écarts nutrition** : mineurs, documentés, acceptables par utilisateur comme compatibles durabilité. Aucun signal d'escalade.

---

### 🟢 POSITIF — Amélioration genou gauche

| Attribut | Valeur |
|----------|--------|
| **Description** | Aucun signal genou S25 observé vs signal léger S24 (2/3 séances RUN-45-EF) |
| **Profil temporel** | S24 : 2 signaux détectés sur 3 séances running. S25 : 0 signal détecté sur 1 séance (RUN-40-EF) |
| **Cause probable** | Réduction charge : RUN-40-EF (vs RUN-45-EF S24), instruction monitoring + réduction immédiate si signal |
| **Impactant positif** | Confirms que ajustement charge running efficace ; genou capable d'adapter si progressivité respectée |
| **Certitude** | **Haute** : amélioration observable, corrélation charge-signal clair |
| **Sustainability** | Bonne : pattern montre adaptabilité système genou |

---

### 🟢 POSITIF — Énergie rapportée améliorée

| Attribut | Valeur |
|----------|--------|
| **Description** | Énergie S25 « plutôt bonne » vs S24 « moyenne-basse » |
| **Profil temporel** | Amélioration relative, corrélée sommeil stable S25 vs baisse S24 |
| **Cause probable** | Récupération sommeil relative (bien que 7h8m < objectif 7h10, quand même +2 min vs S24) ; stress professionnel externe baissé (consigne S25 validée) |
| **Impactant positif** | Compatible continuation Phase 4 sans durcissement ; motivation maintenue |
| **Certitude** | **Moyenne** : autoreport subjectif ; cohérent avec contexte externe (stress baissé) |

---

### 🟢 POSITIF — Timing coucher optimisé

| Attribut | Valeur |
|----------|--------|
| **Description** | Coucher moyen S25 11:42 PM vs S24 12:05 AM = avancé 23 min |
| **Profil temporel** | Amélioration nette ; aligné consigne hygiène sommeil S25 (23h–23h30 cible) |
| **Cause probable** | Hygiène sommeil prioritaire S25, utilisateur actif |
| **Impactant positif** | Confirms capacité à ajuster comportement santé ; fondation pour récupération sommeil améliorer S26 si nuits courtes évitées |
| **Certitude** | **Haute** : donnée mesurée |

---

### 🟢 POSITIF — Conformité activités adaptivement gérée

| Attribut | Valeur |
|----------|--------|
| **Description** | 2/3 séances complétées (66%) ; omission 3e séance (tempo) justifiée par signal lombaire |
| **Profil temporel** | Décision volontaire : utilisateur a arrêté tempo facie signal corpo |
| **Impactant positif** | Demonstrates auto-care et respect contraintes santé ; évite escalade potentielle |
| **Certitude** | **Haute** : choix conscient, documenté |

---

## 3. Tableau synthétique signaux S25

| Gravité | Signal | Profil | Certitude étiologie | Risque escalade |
|---------|--------|--------|-------------------|-----------------|
| 🔴 Majeur | Lombaire escalade (sam–dim, niveau 2) | Tardif, persistant, inexpliqué | Basse (multifactoriel) | Modéré |
| 🟡 Mineur | Volatilité sommeil (nuit 31 jan très courte) | Isolée, cause identifiée | Moyenne | Faible si isolée |
| 🟡 Mineur | Chocolat quotidien | Stable, accepté | Haute | Faible |
| 🟡 Mineur | Alcool weekend élevé | Assumé social | Moyenne-basse | Faible-modéré |
| 🟢 Positif | Genou en amélioration | Aucun signal vs S24 léger | Haute (corrélation charge) | Basse |
| 🟢 Positif | Énergie améliorée | Rapportée bonne vs moyenne-basse | Moyenne | Basse |
| 🟢 Positif | Timing coucher optimisé | Avancé 23 min | Haute | Basse |
| 🟢 Positif | Activités adaptatif gérées | 2/3 complétées, omission justifiée | Haute | Basse |

---

## 4. Synthèse en gravité progressive

### Signaux critiques (demandent surveillance S26 immédiate)
1. **Escalade lombaire sam–dim** (niveau 2, persistant, inexpliqué) : **Monitorer récurrence S26** → si répétition même intensité ou ampleur → signal d'escalade confirmé → nécessité ajustement

### Signaux mineurs (surveillance, pas action immédiate)
2. Volatilité sommeil (nuit 31 jan isolée mais contributrice probable à fatigue) : **Confirmer S26** que pattern isolé ou récurrence ?
3. Écarts nutrition (chocolat, alcool) : **Acceptables** à court-terme ; monitoring si escalade

### Signaux positifs (confirmer S26)
- Genou : trajectory stable, continuer monitoring
- Énergie : stable, corrélée sommeil
- Conformité : adaptative et saine

---

## 5. Incertitudes documentées

1. **Étiologie signal lombaire** : Multifactoriel probable (fatigue neuro, sommeil volatile, Phase 4, ou sous-perception). Aucune falsification locale possible S25 ; clarification requiert monitoring comparatif S26.
2. **Attribution volatilité sommeil → fatigue lombaire** : Plausible mais non-exclusive. Autres vecteurs possibles (cumul fatigue motrice, Phase 4 physiologique, facteur externe).
3. **Perception vs réalité signaux** : Utilisateur reconnaît possibilité mauvaise interprétation. Signaux rapportés = donnée primaire acceptée, mais certitude diagnostique basse.

---

## 6. Questions pour utilisateur (optionnel)

Répondre si tu as 2–3 min. Sinon, tape "continuer" pour Étape 3.

**Q1 : Escalade lombaire sam–dim — CLARIFIÉE**  
Profil mécanique/postural clair : douleur localisée zone lombaire/bassin, déclencheurs identifiés (respiration profonde diaphragmatique, mouvements, marche, posture droite). ✓ Intégré. Hypothèses révisées pour refléter dysfonction posturo-motrice vs simple fatigue musculaire.

**Q2 : Nuit courte 31 jan + énergie S25 — CLARIFIÉE**  
Fatigue légère samedi (attendue), mais impact principal = moral et irritabilité (facteur nerveux/émotionnel possible). ✓ Intégré. Ajoute dimension psycho-émotionnelle à signal lombaire.

**Q3 : Alcool weekend — CLARIFIÉE**  
Type : vin + apéritif anisé (profil modéré, non alcools forts). ✓ Intégré. Réduit risque cumulatif hydratation vs alcools forts.

**A2 mise à jour.** Aucune question supplémentaire. Prêt(e) pour Étape 3 ?
