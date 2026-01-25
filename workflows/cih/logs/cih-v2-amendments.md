# Amendements CIH v2 — Clarifications d'exécution

**Date** : 25 janvier 2026  
**Statut** : Stabilisé  
**Initiateur** : META-GOV-01

---

## Résumé exécutif

Trois ambiguïtés ont été détectées dans le CIH v2 qui induisaient des comportements d'exécution non conformes. Des amendements clarifiants ont été apportés au document principal ([cih.md](cih.md)).

---

## 1. Problème 1 : Ambiguïté sur les artefacts obligatoires (Étape 7)

### Ce qui a été observé
L'agent produisait **soit** le plan concret au bon emplacement (`plan_semaine_XX.md` ou `phase{N}.md`), **soit** l'artefact `A6_PLAN_CONCRET.md`, mais rarement les deux simultanément.

### Racine du problème
La formulation originale :
```
Artefact produit (intermédiaire)
- `/data/phase{N}/S{WW+1}/plan_semaine_{WW+1}.md` ou `/data/phase{N+1}/phase{N+1}.md` (si nouvelle phase)
- et `A6_PLAN_CONCRET.md` (copie du plan généré)
```

Le mot « **ou** » suivi de « **et** » crée une ambiguïté : l'agent interprétait comme une **alternative exclusive** plutôt qu'une conjonction logique avec deux chemins mutuellement exclusifs pour le premier artefact.

### Correction appliquée

**Nouvelle formulation (Étape 7)** :

```
Artefacts produits (DEUX fichiers obligatoires)

1. Plan concret au bon emplacement (en fonction de la décision humaine) :
   - `/data/phase{N}/S{WW+1}/plan_semaine_{WW+1}.md` (si continuité)
   - OU `/data/phase{N+1}/phase{N+1}.md` (si nouvelle phase)

2. Copie locale de synthèse (obligatoire) :
   - `A6_PLAN_CONCRET.md` (stocker dans `/data/phase{N}/S{WW}/analysis/A6_PLAN_CONCRET.md`)

Critère de succès : Les deux fichiers doivent être créés et leurs chemins absolus affichés explicitement.
```

### Impact
- **Clarté** : Pas d'alternative entre les deux artefacts. Les deux doivent être produits.
- **Critère de succès explicite** : L'agent ne peut considérer l'étape 7 comme complète que si **les deux fichiers sont créés**.

---

## 2. Problème 2 : Continuité automatique (Pause obligatoire)

### Ce qui a été observé
L'agent exécutait souvent l'étape N, puis immédiatement l'étape N+1, sans s'arrêter et attendre l'instruction formelle de l'utilisateur.

### Racine du problème
La section 3 (vue d'ensemble) énonce le principe de pause, mais :
- Il ne figure que dans la **vue d'ensemble**, non répété dans les détails des étapes 1–9
- Aucune injonction **explicite d'arrêt** à la fin de chaque étape
- Pas de distinction claire entre « affichage des résultats » et « attente de l'instruction suivante »

### Correction appliquée

**Nouvelle formulation (Section 3)** :

```
Protocole de pause (obligatoire après chaque étape) :
- L'agent affiche clairement le ou les artefacts générés
- L'agent énumère les fichiers créés (chemins absolus)
- L'agent n'initie JAMAIS l'étape suivante sans instruction explicite
- L'utilisateur doit donner l'instruction formelle (e.g. "continuer à l'étape suivante") pour procéder
- Les commentaires ou questions utilisateur sont acceptés avant de passer à l'étape suivante
```

### Impact
- **Gouvernance** : La pause entre étapes devient une **obligation explicite**, non implicite.
- **Traçabilité** : L'énumération des chemins absolus des artefacts crée une checklist vérifiable.
- **Flexibilité** : L'utilisateur peut poser des questions ou ajouter des commentaires sans déclencher l'étape suivante.

---

## 3. Problème 3 : Stockage imprécis des artefacts intermédiaires

### Ce qui a été observé
Le CIH ne précisait pas où stocker les artefacts intermédiaires `A1_...` à `A7_...`. L'agent pouvait supposer qu'il s'agissait d'artefacts « informatiques » non persistés.

### Racine du problème
La section « Artefacts et persistance » distinguait « intermédiaires » et « de référence » sans fournir de règle de **localisation physique** pour les intermédiaires.

### Correction appliquée

**Nouvelle formulation (Section 6)** :

```
Artefacts intermédiaires

Stockage : tous les artefacts intermédiaires (A1–A7) sont créés dans le dossier `/data/phase{N}/S{WW}/analysis/`.
```

### Impact
- **Persistance** : Tous les artefacts (intermédiaires et de référence) sont **persistés sur disque**.
- **Traçabilité** : Permet une inspection et un audit post-CIH des décisions intermédiaires.
- **Cohérence** : Aligne la pratique avec la finalité du CIH : « produire une mémoire exploitable du plan ».

---

## 4. Changements connexes

### Section 8 — Inputs
Clarification des inputs pour l'étape 8 :
- Ancien : `A6_PLAN_CONCRET.md`
- Nouveau : `/data/phase{N}/S{WW}/analysis/A6_PLAN_CONCRET.md`

---

## 5. Récapitulatif des règles mises à jour

| Règle | Avant | Après | Impact |
|-------|-------|-------|--------|
| **Étape 7 – Artefacts** | `ou` + `et` (ambigü) | DEUX fichiers (explicite) | Éliminer les omissions |
| **Pause entre étapes** | Implicite (section 3 uniquement) | Explicite + protocole détaillé | Respecter la gouvernance |
| **Stockage A1–A7** | Non spécifié | `/data/phase{N}/S{WW}/analysis/` | Garantir la persistance |
| **Critère succès Ét. 7** | Implicite | Explicite (les deux fichiers) | Vérifiabilité |

---

## 6. Notes pour l'exécution

1. **Après l'étape 7**, l'agent doit afficher explicitement :
   ```
   Artefacts créés :
   - /data/phase{N}/S{WW+1}/plan_semaine_{WW+1}.md [OU /data/phase{N+1}/phase{N+1}.md]
   - /data/phase{N}/S{WW}/analysis/A6_PLAN_CONCRET.md
   ```

2. **Après chaque étape (1–9)**, l'agent s'arrête et affiche :
   ```
   Étape X complétée. Artefact(s) générés : [liste].
   En attente de l'instruction pour l'étape X+1.
   ```

3. **Aucune continuité automatique** : l'agent attend l'instruction explicite de l'utilisateur.

---

## 7. Validité et persistance

Ces amendements sont **intégrés au CIH v2** et deviennent **normatifs immédiatement**.

Pour toute évolution future, consulter : [meta-gov.md](/roles/meta-gov.md)

