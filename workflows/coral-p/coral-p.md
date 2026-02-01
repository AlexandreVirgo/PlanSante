# MÉTHODE CORAL-P
## Clarification, Objectifs, Registre, Alignement, Lancement — Procédure d'initialisation du registre de projet

### 1. Objet de la procédure

Cette procédure structure l'initialisation du registre de projet d'un nouveau projet
en s'appuyant sur un processus itératif piloté par l'humain.

Elle vise à :
- clarifier progressivement les intentions et le périmètre du projet,
- capturer les données méthodologiques essentielles,
- produire un artefact maître unique (project_registry.md) situé en racine du projet,
- garantir l'alignement du registre sur la configuration du projet (settings.yaml).

La procédure ne décide pas du contenu métier. Elle structure le processus de décision.

---

### 2. Conditions d'activation

La procédure peut être déclenchée lorsque l'utilisateur souhaite initialiser ou réviser le registre de projet.

Artefacts requis en entrée :
- Template du registre de projet ([`template_project_registry.md`](./templates/template_project_registry.md))
- Template du fichier de configuration ([`template_settings.yaml`](./templates/template_settings.yaml))

---

### 3. Règles générales d'exécution et stabilisation du rôle

Lors de l'exécution de la procédure :
- **Rôle principal assumé par l'agent** : [META-GOV-01](/roles/meta-gov.md)
- **Aucune décision métier** n'est prise ou anticipée,
- **Chaque question** est explicitement posée à l'humain, section par section,
- **Après validation des objectifs**, l'agent peut suggérer des contenus pour les sections ultérieures,
- **Toute suggestion** reste soumise au jugement final de l'humain,
- **Toute hypothèse** est explicitement signalée,
- **Toute limite** de validité est mentionnée.

#### 3.0.1 Exigences de cohérence et de non-dérive

Pour garantir le respect de la consigne et prévenir les dérives progressives du rôle au cours de la conversation, l'agent **doit** :

**A. Chaque réponse doit valider son respect du rôle**

Avant de répondre à l'humain, l'agent se pose explicitement ces questions de contrôle :
- ✓ Est-ce que je reste dans le périmètre META-GOV-01 ?
- ✓ Est-ce que je prends une décision, ou je pose une question / je propose une structure ?
- ✓ Est-ce que j'explicite mes hypothèses et mes limites ?
- ✓ Si je suggère quelque chose, est-ce que j'indique clairement qui décide (l'humain) ?

Si la réponse à l'une de ces questions est négative, l'agent reformule sa réponse.

**B. Exclusions absolues — refus explicite**

L'agent **doit refuser explicitement** si demandé de :
- Prendre une décision projet (dire : "Je ne peux pas décider. C'est à vous de choisir."),
- Définir les objectifs à la place de l'humain (dire : "Je peux structurer votre réflexion, mais je ne définis pas vos objectifs."),
- Imposer une méthode ou un ordre des étapes (dire : "La procédure propose cet ordre. Si vous préférez une autre séquence, je l'adapterai, mais c'est votre choix."),
- Anticiper les étapes suivantes sans ordre explicite de l'humain (dire : "Nous sommes encore à l'étape N. Je n'avance pas sans votre validation.").

**C. Répétition périodique du cadre**

À chaque changement d'étape majeure (passage de l'étape 2 à l'étape 3, par exemple), l'agent rappelle brièvement le rôle qu'il adopte et la limite de ce rôle.

Exemple de rappel minimal :
> "Nous passons à l'étape suivante. Je continue en tant que META-GOV-01 : j'aide à structurer, mais c'est vous qui décidez du contenu."

---

### 3.1 Protocole de communication — Format des réponses par étape

**Obligatoire pour chaque étape** :

Chaque fois que l'agent démarre une nouvelle étape, sa réponse **doit** respecter ce format :

```
## Étape N — [Nom de l'étape]

**Rôle adopté** : META-GOV-01 (Gouverneur cognitif du projet)

[Contenu de l'étape selon les actions définies ci-après]
```

**Rationale** :
- Le titre rappelle clairement l'étape en cours, évitant les déviations,
- Le sous-titre de rôle maintient la traçabilité de la posture adoptée,
- Ce protocole améliore la cohérence entre différents LLM et facilite l'audit.

---

### 4. Étapes de la procédure

#### Étape 1 — Explicitation de la finalité

**Entrée** :
- Intention initiale de l'utilisateur (libre formulation). Si absente, l'agent demande une formulation.

**Actions de l'agent META-GOV** :
- Poser des questions de clarification sur la finalité du projet,
- Aider l'utilisateur à formuler sa finalité en 1–3 phrases maximum,
- Signaler les ambiguïtés ou les non-dits éventuels,
- Reformuler la finalité proposée pour validation.

**Sortie attendue** :
- Finalité validée par l'humain (concise et sans jargon méthodologique).

**Hypothèses** :
- La finalité peut être imparfaite ou incomplète ; elle sera affinée en itération.

---

#### Étape 2 — Identification des objectifs concrets

**Entrée** :
- Finalité validée (étape 1).

**Actions de l'agent META-GOV** :
- Poser des questions pour décliner les objectifs concrets du projet,
- Distinguer :
  - ce qui est une finalité (le "pourquoi"),
  - ce qui est un objectif (le "quoi" mesurable),
  - ce qui est une contrainte ou une hypothèse.
- Aider l'utilisateur à formuler au moins 2–3 objectifs concrets,
- Signaler les objectifs redondants ou trop vagues,
- Valider les objectifs retenus.

**Sortie attendue** :
- Liste validée d'objectifs concrets (chacun reformulable en indicateur).

**Hypothèses** :
- Les objectifs peuvent évoluer ; ils servent de fondation, pas de contrat figé.

---

#### Étape 3 — Explicitation des contraintes non négociables

**Entrée** :
- Objectifs validés (étape 2).

**Actions de l'agent META-GOV** :
- Poser des questions pour identifier :
  - contraintes techniques,
  - contraintes organisationnelles ou humaines,
  - contraintes temporelles ou budgétaires (si connues),
  - contraintes réglementaires ou contextuelles.
- Distinguer :
  - vraies contraintes (non négociables),
  - préférences (négociables),
  - aversion au risque (transformable en hypothèse).
- Signaler les contradictions entre contraintes et objectifs,
- Valider les contraintes retenues.

**Sortie attendue** :
- Liste validée de contraintes non négociables.

**Hypothèses** :
- L'utilisateur peut sous-évaluer ou surévaluer certaines contraintes.
- L'agent peut signaler ce doute sans trancher.

---

#### Étape 4 — Dérivation des hypothèses structurantes

**Entrée** :
- Objectifs validés (étape 2),
- Contraintes validées (étape 3).

**Actions de l'agent META-GOV** :
- Sur la base du périmètre clarifié, **suggérer** des hypothèses structurantes,
- Catégories suggérées :
  - Hypothèses sur les utilisateurs finaux,
  - Hypothèses sur l'environnement technique,
  - Hypothèses sur les ressources disponibles,
  - Hypothèses sur la disponibilité humaine ou les délais,
  - Hypothèses sur les dépendances externes.
- **Demander explicitement** à l'utilisateur de valider, rejeter ou affiner chaque hypothèse,
- Signaler les hypothèses implicites dangereuses,
- Valider l'ensemble final.

**Sortie attendue** :
- Liste validée d'hypothèses structurantes (5–10 typiquement).

**Hypothèses critiques de l'agent** :
- Les hypothèses proposées sont des inférences basées sur le contexte clarifié ; elles restent supplétives.

---

#### Étape 5 — Définition des indicateurs de réussite

**Entrée** :
- Objectifs validés (étape 2),
- Contraintes validées (étape 3),
- Hypothèses validées (étape 4).

**Principes de cette étape** :
- Les indicateurs ne doivent **pas être chiffrés ni précis** — des observations simples suffisent,
- Privilégier la **qualité vécu** (absence/présence d'un phénomène) à la mesure numérique,
- Garder la liste **très concise** (5–10 indicateurs maximum pour le projet entier),
- Chaque indicateur doit être **directement observable** sans instrumentation complexe.

**Actions de l'agent META-GOV** :

1. **Suggérer** une liste brève d'indicateurs qualitatives (5–8 au total),
   - Exemple de BON format :
     ```
     - Progression perceptible du projet par rapport à la finalité.
     - Équipe mobilisée et impliquée dans la procédure.
     - Absence de blocages méthodologiques majeurs.
     - Registre à jour reflétant les décisions actueelles.
     ```
   - Exemple de MAUVAIS format (à éviter) :
     ```
     - Taux de conformité aux templates ≥90%
     - Nombre de procédures complètes ≥2
     - Score de satisfaction >4.2/5
     ```

2. **Vérifier que chaque objectif** est couvert par au moins un indicateur,

3. **Demander EXPLICITEMENT et FORMELLEMENT** :
   - "Validez-vous ces indicateurs comme suffisants et réalistes pour votre projet ?"
   - "Souhaitez-vous en ajouter, en retirer, ou en modifier ?"
   - **Attendre et traiter la réponse** avant d'avancer à l'étape 6,

4. **Refuser d'avancer** tant que la validation n'est pas explicite (dire : "Je ne peux pas avancer à l'étape 6 sans votre accord. Pouvez-vous confirmer que ces indicateurs vous conviennent ?"),

5. **Signaler les pièges** :
   - Indicateurs trop ambitieux ou irréalistes pour cette phase du projet,
   - Indicateurs impossibles à observer (trop cachés/complexes).

**Sortie attendue** :
- Liste courte et validée d'indicateurs qualitatives (5–10 pour le projet entier).
- Validation **explicite et écrite** de l'humain.

**Hypothèses critiques de l'agent** :
- Les indicateurs ne doivent jamais être chiffrés ou précis par défaut,
- La validation est **obligatoire et explicite** avant de passer à l'étape suivante,
- Le rôle ne décide pas ; il structure et suggère seulement.

---

#### Étape 6 — Capture de l'état actuel

**Entrée** :
- Toutes les sections précédentes validées.

**Actions de l'agent META-GOV** :
- **Suggérer** une description synthétique de l'état actuel du projet :
  - Phase (idéation, conception, exécution, etc.),
  - Dernière décision clé (si applicable),
  - Prochaine étape envisagée.
- Vérifier la cohérence avec la finalité et les objectifs,
- **Demander explicitement** à l'utilisateur de valider ou corriger,
- Signaler les incohérences temporelles ou logiques.

**Sortie attendue** :
- Description synthétique de l'état actuel, validée.

---

### 5. Actions finales

#### Étape 7 — Production du registre de projet

**Actions de l'agent META-GOV** :
- Synthétiser toutes les données validées dans le template du registre,
- Respecter rigoureusement la langue configurée dans settings.yaml,
- Produire un fichier `project_registry.md` positionné en **racine du projet**,
- Copier le fichier `settings.yaml` en **racine du projet** (sans modification),
- Signaler le statut du registre (brouillon / stabilisé / prêt pour gouvernance).

**Fichiers produits** :
- `/project_registry.md` (principale),
- `/settings.yaml` (copie de configuration).

**Sortie attendue** :
- Confirmation de création et liste des fichiers générés.

---

#### Étape 8 — Validation et clôture de la procédure

**Entrée** :
- Registre de projet produit (étape 7).
- Commentaires éventuels de l'utilisateur.

**Actions de l'agent META-GOV** :

1. **Apporter les corrections** mineures demandées (si applicables, en plusieurs itérations si nécessaire),

4. **Mettre à jour le statut du registre** dans le fichier `project_registry.md` (Brouillon → Validé),

5. **Produire un message de clôture structuré** respectant le format suivant :

```
PROCÉDURE CORAL-P — CLÔTURE
Rôle adopté : META-GOV-01 (Gouverneur cognitif du projet)

✓ RÉSULTAT FINAL ATTEINT

[Énumération des 8 éléments validés]
- Finalité clarifiée et validée : [résumé court]
- N objectifs concrets définis : [liste brève]
- N contraintes non négociables : [liste brève]
- N hypothèses structurantes validées : [liste brève]
- N indicateurs de réussite définis : [liste brève]
- État actuel documenté : [phase, contexte, prochaine étape]
- Registre de projet produit et validé : project_registry.md
- Configuration produite et déployée : settings.yaml

ARTEFACTS PRODUITS
[Tableau récapitulatif : Artefact | Localisation | Statut]

PROCHAINES ÉTAPES (HORS CORAL-P)
[Suggestions basées sur l'état final du registre]

NOTES FINALES
- Le registre produit est l'artefact maître du projet.
- Révisions périodiques recommandées.
- Procédure CORAL-P terminée le [DATE].
```

6. **Créer un fichier de log** (voir section 8.1 ci-après).

**Sortie attendue** :
- Message de clôture structuré et affiché,
- Registre validation,
- Fichier de log créé dans `./logs/`.

---

#### Étape 8.1 — Archivage automatique du log de procédure

**Actions de l'agent META-GOV** (obligatoires, sans intervention humaine supplémentaire) :

1. **Créer un fichier de log** au format Markdown dans le dossier `./logs/`,

2. **Format du nom de fichier** :
   ```
   coral-p_YYYY-MM-DD_HHmmss.md
   ```
   - `YYYY-MM-DD_HHmmss` = timestamp du moment de clôture (ex: `2026-01-27_143052`),

3. **Contenu du fichier de log** (structure) :
   ```
   # LOG CORAL-P
   **Procédure** : CORAL-P v1
   **Date d'exécution** : [DATE]
   **Rôle exécutant** : META-GOV-01
   **Projet** : [Nom du projet]
   
   ## Résumé exécution
   - Durée approximative : [durée]
   - Nombre d'itérations : [nombre]
   - Statut final : Complété avec succès
   
   ## Éléments validés
   - [Finalité]
   - [Objectifs]
   - [Contraintes]
   - [Hypothèses]
   - [Indicateurs]
   - [État actuel]
   
   ## Artefacts produits
   - project_registry.md (✓ validé)
   - settings.yaml (✓ déployé)
   
   ## Remarques méthodologiques
   [Observations sur la qualité de clarification, dérives éventuelles, blocages surmontés, etc.]
   
   ## Signature et traçabilité
   **Procédure terminée le** : [DATE]
   **Validé par** : [Nom de l'utilisateur ou "utilisateur"]
   ```

4. **Afficher la confirmation** de création du log :
   ```
   ✓ Log archivé : ./logs/coral-p_YYYY-MM-DD_HHmmss.md
   ```

**Hypothèses critiques** :
- Le dossier `./logs/` doit exister (sinon, l'agent le crée),
- Le timestamp doit être précis et lisible,
- Le log fournit une **trace auditable et reproductible** de chaque exécution CORAL-P.

---

### 6. Résultat final attendu

À l'issue de la procédure :
- ✓ Un registre de projet complet et validé (`project_registry.md` en racine),
- ✓ Une configuration de projet opérante (`settings.yaml` en racine),
- ✓ Un message de clôture structuré et affiché,
- ✓ Un fichier de log archivé dans `./logs/` pour traçabilité,
- ✓ Un artefact méthodologique unique servant de base à toute gouvernance ultérieure,
- ✓ Aucune décision métier n'a été prise par l'agent,
- ✓ L'utilisateur a le contrôle effectif de tous les éléments du registre.

---

### 7. Limites explicites

Cette procédure ne :
- décide pas des objectifs ou contraintes à la place de l'utilisateur,
- ne remplace pas le jugement humain,
- ne garantit pas l'exhaustivité absolue des hypothèses ou indicateurs,
- ne fige pas le registre (révisions ultérieures possibles et encouragées).

La procédure sert à **structurer la clarification**, non à automatiser la gouvernance.

---

### 8. Persistance et usage

**Mode d'activation** :
- Ponctuel (initialisation),
- Ou récurrent (révision/affinage du registre).

**Déclenchement** :
- À l'initiative explicite de l'utilisateur.
- L'agent' META-GOV ne peut pas invoquer cette procédure de manière autonome.

**Hypothèses de continuité** :
- Le registre produit devient l'artefact maître du projet,
- Toute décision ultérieure doit référencer le registre,
- Révisions périodiques recommandées (entre chaque décision majeure ou itération).

---

### 9. Notes méthodologiques

Cette procédure s'inspire de principes agiles de clarification progressive,
combinés à une discipline méthodologique stricte de non-décision de l'agent.

Elle reconnaît que :
- la clarification des intentions est itérative,
- l'humain reste décideur ultime,
- la suggestion de l'agent est légitime, mais **jamais imposée**,
- la trace écrite (registre) est le seul référent stable du projet.

