# MÉTHODE IRIS-R  
## Identification et Rationalisation des rôles par Invariants de Situation

### 1. Objet de la méthode

IRIS-R est une méthode structurée permettant d’identifier, définir et formaliser
les rôles cognitifs nécessaires à un projet, en s’appuyant sur les besoins réels
de l’utilisateur et les capacités effectives d’un LLM.

La méthode ne crée ni rôles métier décisionnels, ni agents autonomes.
Elle produit exclusivement des rôles cognitifs gouvernables.

---

### 2. Conditions d’activation

La méthode IRIS-R peut être invoquée lorsque :
- un registre de projet est disponible et validé,
- l’utilisateur souhaite identifier ou réviser les rôles utiles au projet,
- aucune décision projet n’est déléguée au LLM.

Artefact requis en entrée :
- Registre de projet (version courante).

---

### 3. Règles générales d’exécution

Lors de l’exécution de la méthode :
- le LLM n’anticipe aucune action suivante,
- le LLM ne propose aucune décision,
- toute hypothèse est explicitement signalée,
- toute limite de validité est mentionnée.

Le LLM agit exclusivement comme **analyste méthodologique**.

---

### 4. Étapes de la méthode

#### Étape 0 — Cadre de référence

- Prendre le registre de projet comme cadre factuel unique.
- Ne pas compléter ni interpréter les informations manquantes.
- Identifier explicitement :
  - finalité,
  - périmètre,
  - contraintes non négociables.

Sortie attendue :
- Rappel synthétique du cadre (si nécessaire).

---

#### Étape 1 — Identification des besoins cognitifs

- Identifier les zones du projet nécessitant :
  - analyse,
  - structuration,
  - exploration,
  - clarification,
  - critique,
  - maintien de cohérence.
- Formuler ces besoins sous forme de tensions cognitives potentielles.

Sortie attendue :
- Liste brute et non structurée de besoins cognitifs.

---

#### Étape 2 — Regroupement par fonctions cognitives

- Regrouper les besoins par fonction cognitive dominante.
- Chaque groupe correspond à un verbe cognitif principal.

Règle :
- Une fonction dominante par groupe.

Sortie attendue :
- Liste de fonctions cognitives candidates.

---

#### Étape 3 — Test de légitimité LLM

Pour chaque fonction candidate, vérifier si elle peut être exercée sans :
- décision engageante,
- interprétation située du réel,
- responsabilité des conséquences.

- Si non → exclure la fonction.
- Si oui → conserver la fonction.

Sortie attendue :
- Liste de fonctions cognitives légitimes pour un LLM.

---

#### Étape 4 — Cristallisation en rôles cognitifs

Pour chaque fonction retenue :
- définir un rôle fonctionnel minimal,
- préciser :
  - finalité,
  - fonctions autorisées,
  - hors-périmètre explicite.

Aucun métier ni persona à ce stade.

Sortie attendue :
- Liste de rôles cognitifs “nus”.

---

#### Étape 5 — Façade métier (optionnelle et gouvernée)

Cette étape est **strictement optionnelle** et vise uniquement à améliorer
l’appropriation humaine des rôles identifiés.

Règles d’application :
- Aucune façade métier n’est ajoutée par défaut.
- Le LLM ne produit jamais de façade métier de sa propre initiative.

Déclenchement possible uniquement dans les cas suivants :
1. L’utilisateur demande explicitement l’ajout d’une façade métier.
2. Le LLM identifie qu’une façade métier pourrait améliorer la lisibilité ou
   l’appropriation des rôles et **le signale sans la produire**, en demandant
   confirmation explicite à l’utilisateur.

Contraintes impératives :
- Toute façade métier est explicitement qualifiée comme
  **« inspiration non normative »**.
- Aucune autorité, responsabilité ou capacité décisionnelle ne peut être
  déduite de la façade métier.
- Les rôles cognitifs restent la référence fonctionnelle unique.

Sortie attendue :
- Soit aucune façade métier.
- Soit une association validée par l’utilisateur entre rôles cognitifs et
  inspirations métier, sans modification des rôles eux-mêmes.


---

#### Étape 6 — Vérification de cohérence

Vérifier que :
- chaque besoin cognitif initial est couvert,
- aucun rôle n’est redondant,
- aucun rôle n’est excessivement large ou étroit.

Ajustements autorisés :
- fusion,
- scission.

Aucun ajout narratif.

---

### 5. Résultat final attendu

- Liste validable de rôles cognitifs.
- Chaque rôle est prêt à être formalisé via une fiche de rôle standard selon le template T6_role.md.
- Les rôles sont explicitement provisoires ou stabilisés selon le contexte projet.

---

### 6. Limites explicites

IRIS-R ne :
- décide pas des rôles à la place de l’utilisateur,
- ne remplace pas le jugement humain,
- ne crée pas d’agents autonomes,
- ne garantit pas l’exhaustivité absolue.

La méthode sert à **structurer**, non à automatiser la gouvernance.
