# CADRE D’ITÉRATION HEBDOMADAIRE (CIH)
## Plan de santé personnalisé — Version étendue

---

## 1. Objet du cadre

Le **Cadre d’Itération Hebdomadaire (CIH)** définit un protocole réutilisable
d’actionnement séquentiel des rôles cognitifs du projet.

Il vise à :
- conduire le projet dans le temps de manière structurée,
- garantir la comparabilité inter-semaines,
- préserver la gouvernance humaine,
- produire une mémoire exploitable du plan,
- rendre le projet **opérationnel** (plans concrets).

Ce cadre :
- **ne décide pas**,
- **ne prescrit pas**,
- **n’automatise aucune action**.

---

## 2. Principes généraux

- Un seul rôle est actif à la fois.
- Chaque rôle :
  - consomme des **inputs explicitement définis**,
  - produit **un artefact identifié**.
- Les artefacts sont classés en :
  - **intermédiaires** (non persistés),
  - **de référence** (persistés après décision humaine).
- La **décision humaine** est un point explicite et non contournable.
- La mémoire du système est assurée **exclusivement par PS-SCR-06**.
- Aucun rôle ne valide le travail d’un autre rôle.

---

## 3. Séquence hebdomadaire standard (vue d’ensemble)

1. PS-ANA-02 — Analyse factuelle  
2. PS-SIG-05 — Détection de signaux faibles  
3. PS-COH-04 — Contrôle de cohérence (amont)  
4. PS-STR-01 — Structuration des constats  
5. PS-DIR-07 — Orientation stratégique cadrée  
6. **Décision humaine explicite**  
7. PS-PLAN-08 — Plan concret (opérationnalisation)  
8. PS-COH-04 — Contrôle de cohérence (aval, optionnel)  
9. PS-SCR-06 — Persistance et traçabilité  

Après l'exécution de **chaque** étape (de 1 à 9), y compris après décision humaine explicite, l'agent **s'arrête obligatoirement** et affiche le(s) artefact(s) produit(s).

**Protocole de pause (obligatoire après chaque étape)** :
- L'agent affiche clairement le ou les artefacts générés
- L'agent énumère les fichiers créés (chemins absolus)
- L'agent n'initie **jamais** l'étape suivante sans instruction explicite
- L'utilisateur doit donner l'instruction formelle (e.g. "continuer à l'étape suivante") pour procéder
- Les commentaires ou questions utilisateur sont acceptés avant de passer à l'étape suivante

L'agent, sur instruction formelle de l'utilisateur, procède à l'étape suivante en respectant les règles définies dans ce cadre.

---

## 3.5 Style de présentation agent (Étapes 1–5)

Pour chaque étape 1–5, l'agent adopte un style de présentation **utilisateur-centric** :

**Après création de l'artefact technique AN** :

1. **Afficher résumé concis** (~200–300 mots, pas le fichier complet) :
   - Synthétiser les findings clés
   - Utiliser langage direct, pas technique
   - Mettre en évidence tensions/signaux majeurs
   - Référencer artefact technique si utilisateur a doute

2. **Poser 2–3 questions clarifiantes optionnelles** :
   - Ciblées sur **lacunes informationnelles critiques** identifiées en étape
   - Format simple : texte libre ou choix cochables
   - Preamble : "Réponds si tu as 2–3 min (optionnel)"

3. **S'arrêter obligatoirement** :
   - Ne jamais initier étape suivante sans instruction utilisateur explicite
   - Attendre feedback utilisateur (réponses aux questions ou "continuer")

4. **Raffinage optionnel** :
   - Si utilisateur fournit feedback pertinent → raffiner AN partiellement
   - Documenter feedback brièvement dans artefact ou notes
   - Continuer seulement après instruction utilisateur claire

**Format réponse agent** :

```
## [Étape N] — [Titre rôle]

[Résumé synthétique : 200–300 mots]

### Questions clarifiantes (optionnel)
Q1 : [Question 1]
Q2 : [Question 2]
Q3 : [Question 3]

Répondre si tu as 2–3 min, sinon tape "continuer".

**Artefact technique complet** (optionnel si tu doutes) : [A{N}_...]
```

---

## 4. Détail par étape

---

### Inputs utilisés dans plusieurs étapes
- Registre de projet ([project_registry.md](/project_registry.md))
- Phase en cours (data/phase{N}/phase{N}.md from [project_registry.md § État actuel](/project_registry.md#état-actuel))
- Plan de la semaine écoulée (data/phase{N}/S{WW}/plan_semaine_WW.md)
- Bilan hebdomadaire utilisateur (data/phase{N}/S{WW}/bilan_semaine_WW.md)
- Artefact de référence précédent : R_HEBDO_S{WW-1}.md (si disponible, pour comparaison baseline et contexte tendu)
- Données historiques complètes ([weight_history.csv](/data/weight_history.csv) & [sleeping_history.csv](/data/sleeping_history.csv))
- Données et fichiers de tracking spécifiques à la semaine (fichiers .csv ou autres mentionnés dans bilan, ex. Sommeil.csv)

### Étape 1 — PS-ANA-02 : Analyse du bilan hebdomadaire

**Rôle principal** : [PS-ANA-02](/roles/ps-ana-02.md)

**Inputs attendus**
- Registre de projet
- Phase en cours
- Plan de la semaine écoulée (S{WW})
- Bilan hebdomadaire utilisateur (S{WW})
- Artefact de référence précédent : R_HEBDO_S{WW-1}.md (si disponible)
- Données historiques complètes ([weight_history.csv](/data/weight_history.csv) & [sleeping_history.csv](/data/sleeping_history.csv))
- Fichiers de tracking mentionnés dans bilan (ex. Sommeil.csv, si applicable)

**Artefact produit (intermédiaire)**
- `A1_ANALYSE_HEBDO.md`

**Contenu minimal**
- Tendances observées
- Comparaisons temporelles **quantifiées** (S{WW-1} vs S{WW} pour poids, sommeil, et tout indicateur prioritaire signalé dans plan S{WW})
- Variations notables
- Hypothèses et biais signalés

**Règle d'exhaustivité des données**
- Tout fichier `.csv` listant données historiques (weight_history.csv, sleeping_history.csv) **DOIT** être ouvert, consulté et analysé de manière comparative (S{WW-1} vs S{WW}).
- Tout fichier de tracking spécifique mentionné dans le bilan (ex. Sommeil.csv) **DOIT** être ouvert et exploité, particulièrement si le plan S{WW} insiste sur ce critère comme prioritaire.
- Absence d'exploitation documentée ou explicite = dette analytique signalée clairement en section « Biais et limitations ».
- Les comparaisons doivent porter sur les **données mesurées**, non sur les auto-évaluations qualitatives seules, sauf si donnée quantifiée indisponible (auquel cas, noter la limitation).

**Protocole présentation utilisateur (obligatoire)**
- Agent affiche résumé synthétique (200–300 mots) des findings clés (pas le fichier A1 complet)
- Agent pose 2–3 questions clarifiantes sur lacunes informationnelles (ex : contexte événement, hypothèse utilisateur)
- Preamble : "Réponds si tu as 2–3 min (optionnel)"
- Agent s'arrête et attend feedback utilisateur (réponses ou "continuer")
- Si feedback pertinent → agent raffine A1 optionnellement
- Agent n'initie Étape 2 que sur instruction utilisateur explicite

---

### Étape 2 — PS-SIG-05 : Signaux faibles

**Rôle principal** : [PS-SIG-05](/roles/ps-sig-05.md)

**Inputs attendus**
- `A1_ANALYSE_HEBDO.md`
- Bilan brut utilisateur (ressenti, fatigue, irritants). Si absent, demander à l’utilisateur, puis reprendre l’étape 2.

**Artefact produit (intermédiaire)**
- `A2_SIGNAUX_FAIBLES.md`

**Contenu minimal**
- Liste de signaux détectés
- Niveau d’incertitude associé
- Absence de diagnostic ou conclusion

**Protocole présentation utilisateur (obligatoire)**
- Agent affiche résumé synthétique (200–300 mots) : signaux détectés par gravité (majeur/mineur/positif)
- Agent pose 2–3 questions clarifiantes sur étiologie/causation (ex : hypothèse utilisateur sur cause signal)
- Preamble : "Réponds si tu as 2–3 min (optionnel)"
- Agent s'arrête et attend feedback utilisateur
- Si feedback pertinent → agent raffine A2 optionnellement
- Agent n'initie Étape 3 que sur instruction utilisateur explicite
---

### Étape 3 — PS-COH-04 : Contrôle de cohérence (amont)

**Rôle principal** : [PS-COH-04](/roles/ps-coh-04.md)

**Inputs attendus**
- Registre de projet
- Phase en cours
- Plan de la semaine écoulée
- `A1_ANALYSE_HEBDO.md`
- `A2_SIGNAUX_FAIBLES.md`

**Artefact produit (intermédiaire)**
- `A3_COHERENCE_AMONT.md`

**Contenu minimal**
- Incohérences potentielles
- Tensions logiques identifiées
- Aucun jugement d’opportunité

**Protocole présentation utilisateur (obligatoire)**
- Agent affiche résumé synthétique (200–300 mots) : tableau cohérences + incohérences identifiées
- Agent pose 2–3 questions clarifiantes sur validation incohérences (ex : lien causal, acceptabilité)
- Preamble : "Réponds si tu as 2–3 min (optionnel)"
- Agent s'arrête et attend feedback utilisateur
- Si feedback pertinent → agent raffine A3 optionnellement
- Agent n'initie Étape 4 que sur instruction utilisateur explicite
---

### Étape 4 — PS-STR-01 : Structuration des constats

**Rôle principal** : [PS-STR-01](/roles/ps-str-01.md)

**Inputs attendus**
- `A1_ANALYSE_HEBDO.md`
- `A2_SIGNAUX_FAIBLES.md`
- `A3_COHERENCE_AMONT.md`

**Artefact produit (intermédiaire)**
- `A4_SYNTHESE_STRUCTUREE.md`

**Contenu minimal**
- État synthétique de la semaine
- Tensions structurantes
- Questions ouvertes
- Cadres formels mobilisables

**Protocole présentation utilisateur (obligatoire)**
- Agent affiche résumé synthétique (300–400 mots) : tableau état global + tensions majeures formulées
- Agent pose 3 questions clarifiantes **CRITIQUES** (directement impactent Étape 5 — options stratégiques)
  - Q1 : Hypothèse utilisateur sur étiologie majeure (détermine options)
  - Q2 : Acceptabilité escalade/incohérence observée
  - Q3 : Priorités relatives (ex : poids vs santé)
- Preamble : "Réponds si tu as 3–5 min (optionnel, mais très utile pour étape suivante)"
- Agent s'arrête et attend feedback utilisateur
- Si feedback pertinent → agent raffine A4 optionnellement, mais **surtout intègre feedback en A5**
- Agent n'initie Étape 5 que sur instruction utilisateur explicite

---

### Étape 5 — PS-DIR-07 : Orientation stratégique cadrée

**Rôle principal** : [PS-DIR-07](/roles/ps-dir-07.md)

**Inputs attendus**
- Registre de projet
- Phase en cours
- `A4_SYNTHESE_STRUCTUREE.md`

**Artefact produit (intermédiaire)**
- `A5_OPTIONS_STRATEGIQUES.md`

**Contenu minimal**
- **Option 0 : continuité stricte** (par défaut)
- 1 à 3 options alternatives
- Conditions, implications, risques
- Décision explicitement laissée à l’humain

**Protocole présentation utilisateur (obligatoire)**
- Agent affiche résumé synthétique (400–500 mots) : 3 options stratégiques présentées concisement
  - Description brève chaque option
  - Conditions activation
  - Avantages/risques bullétés
- Agent pose 1 question optionnelle : "Quelle option résonne avec toi intuitivement ?"
  - Ou directement : utilisateur prêt à décider Étape 6
- Preamble : "Lis les 3 options attentivement. Décision Étape 6 proche."
- Agent s'arrête et attend feedback utilisateur OU demande: "Prêt(e) pour Étape 6 (décision) ?"
- Agent n'initie Étape 6 que sur instruction utilisateur explicite
---

### Étape 6 . Décision humaine explicite (obligatoire)

À partir de `A5_OPTIONS_STRATEGIQUES.md`, l’humain décide explicitement :
- de l’état de la phase (poursuite / prolongement / clôture),
- de l’option stratégique retenue,
- du périmètre du plan suivant (hebdomadaire ou phase).

A ce stade, expliciter à l'humain qu'il doit faire un choix clair et formel pour continuer.
Aucune décision n’est implicite.  
Aucun rôle cognitif ne valide ce choix.

---

### Étape 7 — PS-PLAN-08 : Plan concret (opérationnalisation)

**Rôle principal** : [PS-PLAN-08](/roles/ps-plan-08.md)

**Inputs attendus**
- Décision humaine explicite
- Phase en cours ou nouvelle phase validée
- Registre de projet
- Contraintes non négociables ([project_registry.md § Contraintes non négociables](/project_registry.md#contraintes-non-négociables))
- Registre d'activités ([activities_registry.md](/activities/activities_registry.md))

**Artefacts produits (DEUX fichiers obligatoires)**

1. **Plan concret au bon emplacement (en fonction de la décision humaine)** :
   - `/data/phase{N}/S{WW+1}/plan_semaine_{WW+1}.md` (si continuité : semaine suivante de la phase en cours)
   - OU `/data/phase{N+1}/phase{N+1}.md` (si nouvelle phase)

2. **Copie locale de synthèse (obligatoire)** :
   - `A6_PLAN_CONCRET.md` (stocker dans `/data/phase{N}/S{WW}/analysis/A6_PLAN_CONCRET.md`)

**Critère de succès de l'étape 7** : Les deux fichiers doivent être créés et leurs chemins absolus affichés explicitement.

**Règles impératives**
- Le plan généré respecte strictement :
  - [`template_plan_semaine.md`](/workflows/cih/templates/template_plan_semaine.md) **ou**
  - [`template_phase.md`](/workflows/cih/templates/template_phase.md)
- Aucune adaptation du template
- Aucune alternative stratégique proposée
- Les activités sélectionnées doivent être justifiées par référence au registre d'activités et respecter les règles de co-occurrence (cf. [`activities_registry.md`](/activities/activities_registry.md) § 5).
- Tout gap dans le registre (impossibilité de sélectionner une activité répondant aux critères) doit être signalé explicitement, sans création autonome de nouvelle activité.

---

### Étape 8 — PS-COH-04 : Contrôle de cohérence (aval, optionnel)

**Rôle principal** : [PS-COH-04](/roles/ps-coh-04.md)

**Objectif**
Vérifier que le plan concret :
- respecte le registre,
- ne viole aucune contrainte non négociable,
- est cohérent avec la décision humaine.

**Inputs attendus**
- Décision humaine
- `/data/phase{N}/S{WW}/analysis/A6_PLAN_CONCRET.md` (ou le chemin généré à l'étape 7)
- Registre de projet

**Artefact produit (intermédiaire, optionnel)**
- `A7_COHERENCE_EX_POST.md`

**Règle**
- Aucun blocage
- Aucun arbitrage
- Signalement uniquement

---

### Étape 9 — PS-SCR-06 : Persistance et mémoire

**Rôle principal** : [PS-SCR-06](/roles/ps-scr-06.md)

**Inputs attendus**
- Décision humaine
- Plan concret validé
- Éventuel contrôle de cohérence ex post

**Artefacts de référence produits**
- `R_HEBDO_Sxx.md`
- Mise à jour :
  - du plan hebdomadaire,
  - de l’état de la phase,
  - du registre de projet (si requis)

**Règle**
- Documentation fidèle
- Aucune interprétation

---

## 6. Artefacts et persistance

### Artefacts intermédiaires

**Stockage** : tous les artefacts intermédiaires (A1–A7) sont créés dans le dossier `/data/phase{N}/S{WW}/analysis/`.

Liste :
- A1_ANALYSE_HEBDO.md
- A2_SIGNAUX_FAIBLES.md
- A3_COHERENCE_AMONT.md
- A4_SYNTHESE_STRUCTUREE.md
- A5_OPTIONS_STRATEGIQUES.md
- A6_PLAN_CONCRET.md (copie du plan concret généré à l'étape 7)
- A7_COHERENCE_EX_POST.md (optionnel, seulement si étape 8 exécutée)

### Artefacts de référence
- **R_HEBDO_Sxx.md** (créé à l'étape 9, stocké à `/data/phase{N}/S{WW}/`)
- **plan_semaine_{WW+1}.md** ou **phase{N+1}.md** (créé à l'étape 7 au bon emplacement)
- Registre de projet versionné
- État de la phase mis à jour

---

## 7. Statut du cadre

- **Statut** : stabilisé (CIH v2)
- **Révision** : décision humaine uniquement
- **Évolution** : via IRIS-R
- **Dernière intégration** : Registre d'activités (25 janv 2026, cf. [`iris-r_execution_activites.md`](/workflows/iris-r/logs/iris-r_execution_activites.md))

---

## 8. Rappel de gouvernance

- Aucun rôle ne décide.
- Aucun rôle ne valide.
- Le cadre structure, l’humain gouverne.

Ce CIH vise à rendre le projet **pensable, pilotable et applicable** dans la durée.
