# IRIS-R — Exécution : Gap activités physiques

## Date d'exécution
25 janvier 2026

## Contexte
Demande d'intégration du référentiel d'activités physiques dans le CIH pour permettre :
- La sélection explicite des activités basée sur le référentiel,
- La détection de besoins de création de nouvelles séances,
- La traçabilité des choix d'activités.

---

## Résultat de l'analyse

### Besoins cognitifs identifiés
1. **Sélection d'activités** : Traduire une décision stratégique en ensemble cohérent d'activités du référentiel.
2. **Détection de gaps** : Reconnaître quand le référentiel est insuffisant.
3. **Validation de cohérence** : Vérifier que l'ensemble respecte les contraintes non négociables (progressivité, santé, phase).
4. **Traçabilité** : Documenter pourquoi telle activité a été sélectionnée.

### Fonctions cognitives légitimes pour LLM
✅ Toutes les quatre fonctions sont légitimes (critères de test IRIS-R § 3 respectés).

### Rôles et artefacts recommandés

#### Option retenue : Enrichissement de PS-PLAN-08 + création index statique

**Justification** :
- Zéro impact structurel sur CIH (reste 9 étapes),
- Index dispo pour toute analyse future,
- PS-PLAN-08 reste monofocalé (opérationnalisation),
- Traçabilité intégrée au plan généré.

---

## Modifications implémentées

### 1. Création : `activities_registry.md`

**Localisation** : `activities/activities_registry.md`

**Contenu** :
- Vue par type (running / fullbody) avec métadonnées complètes (durée, RPE, objectif, compatibilité phase).
- Vue par intensité (RPE 1–2 à 6–7).
- Vue par contexte de phase (Phase 1–4 avec ✅/⚠️/❌).
- Matrice de sélection (5 scénarios courants).
- Règles de co-occurrence (7 règles critiques).
- Gaps détectés (suggestions futures).

**Mainteneurs** : PS-PLAN-08 (utilisation), PS-SCR-06 (persistance lors création/modification activité).

**Usage** : 
- PS-PLAN-08 interroge le registre lors de la sélection,
- Documentation justificative de chaque choix,
- Signalement des besoins de création.

---

### 2. Enrichissement : `ps-plan-08.md`

**Modifications** :

#### § 3 — Fonctions cognitives autorisées
✅ Ajout :
- Sélection d'activités physiques du référentiel selon critères,
- Validation de cohérence des activités contre les contraintes,
- Détection de besoins de création de nouvelles activités (signalement seul).

#### § 6 — Nature des entrées attendues
✅ Ajout :
- Registre d'activités (`activities_registry.md`),
- Bilan de la semaine écoulée (pour validation post-exécution).

#### § 7 — Nature des sorties attendues
✅ Ajout subsection : "Sélection d'activités physiques" avec processus explicite (5 étapes) et validation de cohérence.

#### § 9 — Critères d'évaluation du rôle
✅ Ajout 3 critères :
- Activités justifiées par référence au registre,
- Règles de co-occurrence respectées ou signalées,
- Gaps dans le registre signalés (sans création autonome).

---

### 3. Modification : `cih.md`

**Modification § 4.7** (Étape 7 — PS-PLAN-08) :

✅ Ajout input : Registre d'activités.

✅ Ajout règles impératives :
- Activités sélectionnées doivent être justifiées par référence au registre,
- Règles de co-occurrence respectées,
- Gaps signalés explicitement.

---

## État du projet post-implémentation

| Artefact | Statut | Impact |
|----------|--------|--------|
| `activities_registry.md` | ✅ Créé | Index de référence (nouvelle entrée du CIH) |
| `ps-plan-08.md` | ✅ Enrichi | Intègre sélection + validation activités |
| `cih.md` (§ 4.7) | ✅ Modifié | Input nouveau, règles intégrées |
| CIH global | ✅ Stable | 0 changement structurel, 9 étapes inchangées |
| Autres rôles | ✅ Inchangés | Aucun impact |

---

## Prochaines étapes possibles (optionnelles)

### Court terme (applicable immédiatement)
- Tester l'intégration sur la prochaine itération CIH (S25).
- Documenter les cas d'usage réels dans R_HEBDO.
- Évaluer la complétude du registre et les gaps détectés.

### Moyen terme
- Création de fiches activité pour les gaps identifiés (ex: FB-15-MOBI-V1, RUN-25-MICRO-V1).
- Affinage des matrices de sélection basé sur l'expérience.

### Long terme
- Enrichissement du registre avec nouvelles dimensions (ex: équipement, lieu).
- Intégration optionnelle d'un processus d'évaluation activité (ex: "quelles activités ajouter lors d'une nouvelle phase ?").

---

## Notes de gouvernance

- **Aucun rôle nouveau créé** : l'enrichissement de PS-PLAN-08 réintègre les fonctions détectées par IRIS-R.
- **CIH inchangé structurellement** : garantit la stabilité du cadre.
- **Index statique** : maintenable par PS-SCR-06 lors de création/modification activité.
- **Traçabilité assurée** : chaque plan généré documentera sa sélection d'activités.

Cette implémentation respecte les principes du projet :
- ✅ Gouvernance humaine préservée (aucune décision déléguée à plus d'autonomie),
- ✅ Rôles distincts (PS-PLAN-08 opérationnalise, ne décide pas),
- ✅ Mémoire par design (registre + plans générés + R_HEBDO),
- ✅ Scalabilité (peut accueillir nouveaux artefacts ou rôles sans casser CIH).

