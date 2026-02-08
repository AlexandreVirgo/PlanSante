# A3_COHERENCE_AMONT — Semaine 26

## Métadonnées
- **Semaine analysée** : S26
- **Période couverte** : 2 février – 8 février 2026
- **Rôle exécuteur** : PS-COH-04 (Contrôle de cohérence amont)
- **Date génération** : 8 février 2026
- **Artefacts sources** : A1_ANALYSE_HEBDO.md, A2_SIGNAUX_FAIBLES.md, plan_semaine_26.md, project_registry.md, phase4.md, R_HEBDO_S25.md

---

## 1. Cadre de cohérence

**Objectif** : Identifier incohérences potentielles entre :
- **Exécution S26** (faits observés, signaux)
- **Plan S26** (objectifs, modulations Option 1, triggers)
- **Registry projet** (contraintes non-négociables, hypothèses, indicateurs)
- **Phase 4** (objectifs, règles, critères réussite)

**Codification tensions** :
- 🔴 **Critique** : Violation directe contrainte non-négociable OU précurseur d'escalade vers violation
- 🟡 **Mineure** : Déviation observable, impactant moyen ou long-terme, non-violation directe
- 🟢 **Conforme** : Exécution cohérente avec plan/registry/phase

**Aucun jugement d'opportunité** : rôle PS-COH-04 = détection logique, pas arbitrage.

---

## 2. Cohérences validées

### 🟢 Objectif sommeil S26 (priorité absolue) atteint

**Assertion** : Plan S26 fixe un objectif ferme : sommeil moyen > 7h10 (non-négociable). S26 observé : 7h41.

**Vérification** :
- Plan S26 : « Objectif ferme : Sommeil moyen S26 > 7h10 min ✓ NON-NÉGOCIABLE »
- Données : sleeping_history.csv = 7h41 (Fév. 2-8)

**Cohérence** : ✓ **VALIDE**. Objectif prioritaire du plan respecté. Contribue à la contrainte projet « priorité à la santé » (récupération).

---

### 🟢 Modulation préemptive prudente respectée (structure et volumes)

**Assertion** : S26 est une semaine test de modulation (réduction cumul, spacing, durées réduites FB/EF).

**Vérification** :
- FB : réalisé avec séries réduites et ajout pont fessier, RPE 5 (cible 5–6)
- EF : réalisé 35 min (durée modulée), RPE 3 (cible 3–4)
- Spacing : lun/jeu/sam conforme plan

**Cohérence** : ✓ **VALIDE**. Exécution cohérente avec l’intention de modulation et la règle de progressivité.

---

### 🟢 Conformité nutrition Phase 4 (continuity)

**Assertion** : Plan S26 = continuité Phase 4 stricte, aucun changement. Bilan : consignes respectées, week-end plus copieux.

**Vérification** :
- Phase 4 : déficit modéré, pas de durcissement, tolérance vie sociale
- Poids : léger recul calculé S25→S26 (-0.2 kg), compatible

**Cohérence** : ✓ **VALIDE**. Pas d’incohérence majeure constatée entre cadre nutrition et résultats.

---

## 3. Incohérences potentielles détectées

### 🔴 CRITIQUE — Séance tempo au-dessus de la cible vs objectif santé lombaire

**Assertion** : Plan S26 (Option 1 prudente) vise explicitement à protéger la santé lombaire et à contrôler l’intensité de la séance qualité (RPE cible 6, pas d’accélération progressive).

**Faits observés** :
- Tempo : 46 min (vs 40), RPE 6–7 (vs 6), FC max 191
- Signal lombaire : apparition légère au bloc 2, montée progressive sur blocs 3–4 jusqu’à 2/4, samedi soir 2/4
- Retour à 0 le lendemain matin (transitoire)

**Incohérence logique** :
- Plan S26 = modulation prudente + monitoring lombaire + alternative si escalade
- Exécution tempo = intensité initiale trop élevée (départ rapide) + signal lombaire associé
- Registry : contrainte non-négociable « ne pas dégrader la santé lombaire »

**Gravité** : 🔴 **CRITIQUE** (précurseur). Pas de violation persistante (signal transitoire), mais pattern « dérive d’intensité sur qualité → lombaire » menace directement la contrainte projet.

---

### 🟡 MINEURE — Trigger omission TEMPO non activé vs signaux mineurs

**Assertion** : Plan S26 définit un trigger : « si signal niveau 1+ persiste jeudi soir → omission TEMPO samedi ».

**Faits observés** :
- EF (jeudi) : léger signal lombaire rapporté, mais état du soir jeudi dans le bilan = 0 ("Jeudi: matin 0, soir 0")

**Cohérence** : ✓ logique respectée si (et seulement si) le signal ne persistait pas jeudi soir.

**Clarification utilisateur** : le signal lombaire lié à l’EF s’est **vite dissipé après la séance**.

**Incertitude** : La granularité “pendant séance” vs “soir” devient cohérente avec « jeudi soir 0 » (signal transitoire).

**Gravité** : 🟡 **MINEURE** (ambiguïté de granularité, pas une contradiction certaine).

---

### 🟡 MINEURE — Hygiène sommeil (cible coucher) vs contraintes de vie

**Assertion** : Plan S26 poussait un coucher 23h–23h30 strict.

**Faits observés / clarification** :
- Deux couchers tardifs (00:34, 01:17) choisis, week-end
- Pattern structurel : lever semaine ~6h et préférence de ne pas se coucher avant 23h

**Clarification utilisateur** : schéma actuel avec target coucher **22h30/23h** fonctionne bien (énergie moyenne plus élevée sur 2 dernières semaines).

**Incohérence logique** :
- La contrainte de lever tôt en semaine (~6h) + préférence de ne pas se coucher trop tôt crée une tension structurelle.
- Toutefois, le target 22h30/23h est jugé **fonctionnel** et compatible avec une énergie améliorée (ce qui réduit la gravité de la tension).

**Gravité** : 🟡 **MINEURE**. Ce n’est pas une violation du registry (durabilité/autonomie). Tension à surveiller surtout si la durée de sommeil en semaine devient insuffisante.

---

### 🟡 MINEURE — Genou gauche latéral externe : signal mécanique isolé

**Assertion** : Plan S26 demande monitoring genou gauche (réduire intensité si signal).

**Faits observés / clarification** :
- Signal léger en EF, côté extérieur, disparaît après, impression de survenue surtout à allure très lente

**Cohérence** : Le monitoring est respecté (signal identifié), mais l’apparition même du signal est un écart vs l’intention « genou stable ».

**Gravité** : 🟡 **MINEURE** (isolé, transitoire, non escalade).

---

## 4. Synthèse tensions structurantes

| Tension | Gravité | Nature logique | Impact immédiat | Risque escalade |
|---------|---------|----------------|-----------------|-----------------|
| Tempo au-dessus cible ↔ santé lombaire | 🔴 Critique | Plan prudence vs exécution qualité | Signal transitoire, mais associé séance | Faible–modéré si répétition |
| Trigger omission TEMPO ↔ granularité signal | 🟡 Mineure | Ambiguïté “signal en séance” vs “soir” | Décision tempo cohérente si soir=0 | Faible |
| Coucher strict ↔ contraintes semaine/week-end | 🟡 Mineure | Plan hygiène vs préférences/lever 6h | Durée ok, mais transférabilité | Modéré long-terme |
| Genou latéral externe en EF | 🟡 Mineure | Signal isolé vs stabilité attendue | Disparaît après, pas escalade | Faible |

---

## 5. Validations de cohérence réussies (positives)

- ✓ Sommeil > 7h10 atteint (objectif prioritaire respecté)
- ✓ Modulations de durée/spacing appliquées sur FB et EF
- ✓ Adhérence nutrition cadre Phase 4 globalement cohérente
- ✓ Auto-régulation partielle tempo (2 derniers blocs plus adaptés)
- ✓ Signaux lombaires non persistants (retour à 0 le lendemain) = cohérent avec prudence globale

---

## 6. Points de vigilance prioritaires pour Étape suivante

1. **Tension principale** : séance qualité (tempo) = point de fragilité mécanique (lombaire) si intensité dérive au-dessus de la cible.
2. **Tension structurelle** : objectif “coucher tôt strict” vs contrainte lever semaine + préférence de coucher ≥23h (durabilité / transférabilité).
3. **Signal mineur** : genou latéral externe en EF, transitoire — à surveiller pour voir si pattern à allure lente.

---

## 7. Aucun jugement d'opportunité

Rôle PS-COH-04 : **détection logique uniquement**. Pas d’arbitrage, pas de recommandation stratégique.

Incohérences identifiées = **inputs** pour Étape 4 (PS-STR-01) et Étape 5 (PS-DIR-07).
