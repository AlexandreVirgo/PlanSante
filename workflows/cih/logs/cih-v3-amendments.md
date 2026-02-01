# CIH v3 AMENDMENTS — RÉSUMÉ DES MODIFICATIONS
## Passage de CIH v2 (agent-centric) à CIH v3 (human-centric)

**Date** : 1er février 2026  
**Statut** : Intégré dans [cih.md](cih.md)

---

## 1. Principe général

**CIH v2** : Agent produit artefacts denses → utilisateur lit complet pour valider → étape suivante

**CIH v3** : Agent produit artefacts denses + affiche résumé synthétique → utilisateur lit résumé + répond optionnellement → agent raffine si nécessaire → étape suivante

---

## 2. Modifications formelles dans CIH

### **A. Section nouvelle : § 3.5 "Style de présentation agent"**

**Ajout** : Directive générale pour tous les étapes 1–5 :
- Afficher résumé concis (~200–300 mots), pas le fichier complet
- Poser 2–3 questions clarifiantes optionnelles
- S'arrêter obligatoirement (pas d'initiation étape suivante sans instruction)
- Raffiner artefact si feedback utilisateur
- Format : résumé textuel + questions + preamble optionnel

### **B. Modifications Étape 1 (PS-ANA-02)**

**Avant** : 
```
Contenu minimal
- Tendances observées
- Comparaisons temporelles
- Variations notables
- Hypothèses et biais signalés
```

**Après** : Idem + 
```
Protocole présentation utilisateur (obligatoire)
- Agent affiche résumé synthétique (200–300 mots)
- Agent pose 2–3 questions clarifiantes
- Preamble : "Réponds si tu as 2–3 min (optionnel)"
- Agent s'arrête et attend feedback utilisateur
- Si feedback → raffine A1 optionnellement
- Agent n'initie Étape 2 sauf instruction explicite utilisateur
```

### **C. Modifications Étape 2 (PS-SIG-05)**

Même structure que Étape 1 :
- Résumé synthétique de signaux (par gravité majeur/mineur/positif)
- 2–3 questions sur étiologie/causation
- Pause obligatoire, raffinage optionnel

### **D. Modifications Étape 3 (PS-COH-04)**

Même structure :
- Résumé cohérences + incohérences
- 2–3 questions sur validation incohérences
- Pause obligatoire

### **E. Modifications Étape 4 (PS-STR-01)**

Même structure, mais questions sont **CRITIQUES** (impactent directement Options Étape 5) :
- Résumé état global + tensions majeures
- 3 questions clés : étiologie, acceptabilité, priorités
- Preamble renforcé : "...très utile pour étape suivante"
- Pause obligatoire

### **F. Modifications Étape 5 (PS-DIR-07)**

Même structure :
- Résumé 3 options présentées concisement
- 1 question optionnelle (intuition utilisateur)
- Preamble : "Lis attentivement. Décision Étape 6 proche."
- Pause obligatoire avant Étape 6

---

## 3. Suppression templates intermédiaires SN

**Abandon** : Templates `template_S1_..._S5_RESUME_UTILISATEUR.md` ne sont **PAS des artefacts créés**.

**Raison** : 
- Surcharge fichiers (15 fichiers par semaine au lieu de 9)
- Complexité inutile (résumé = contenu textuel en réponse agent)
- Utilisateur n'a pas besoin de fichier intermédiaire

**Archivage** :
- Templates restent en `/workflows/cih/templates/` à titre **référence structuration réponse**
- Agent peut s'en inspirer pour formuler résumés (guide de contenu)
- Pas de fichier SN créé/stocké

---

## 4. Artefacts persistants (inchangés)

Chaque semaine S{WW} :
- ✓ A1_ANALYSE_HEBDO.md
- ✓ A2_SIGNAUX_FAIBLES.md
- ✓ A3_COHERENCE_AMONT.md
- ✓ A4_SYNTHESE_STRUCTUREE.md
- ✓ A5_OPTIONS_STRATEGIQUES.md
- ✓ A6_PLAN_CONCRET.md (Étape 7)
- ✓ A7_COHERENCE_EX_POST.md (Étape 8, optionnel)
- ✓ R_HEBDO_Sxx.md (Étape 9)

**Pas d'ajout** : S1, S2, S3, S4, S5, S1_FEEDBACK, etc.

---

## 5. Protocole utilisateur (simplifié)

**Avant** :
```
User : "Execute CIH"
Agent : [Crée A1, A2, ..., A5]
        "Étapes 1–5 complétées"
User : [Doit lire tous les artefacts]
       "Je choisis Option X" (Étape 6)
```

**Après** :
```
User : "Execute CIH"
Agent : Étape 1
        [Crée A1]
        [Affiche résumé S1 synthétique]
        [Pose Q1, Q2, Q3]
        "Réponds optionnellement ou type 'continuer'"
User : "Q1 : ..., Q2 : ..."
Agent : [Raffine A1 optionnellement]
        "Prêt(e) pour Étape 2 ?"
User : "Continuer"
Agent : Étape 2
        [...idem...]
        
[Itération rapide : 2–3 min/étape au lieu de 2h lecture totale]

User : [À Étape 5]
       [Lis résumé 3 options]
       "Je choisis Option 1"
Agent : Étape 6 (Décision)
```

---

## 6. Bénéfices CIH v3

| Critère | CIH v2 | CIH v3 |
|---|---|---|
| **Charge utilisateur** | Lire 5 artefacts denses (2h) | Lire résumés synthétiques (15 min) |
| **Timing feedback** | Étape 6 seulement | Continu, opportuniste après chaque étape |
| **Qualité analyse** | Complète, peut ignorer contexte utilisateur | Enrichie par feedback progressif |
| **Implication utilisateur** | Minimal jusqu'à décision | Maximal, co-analyse |
| **Traçabilité** | ✓ (artefacts denses) | ✓ (artefacts denses + pratiques utilisateur) |
| **Fichiers créés/semaine** | 9 artefacts (A1–A7, R_HEBDO) | 9 artefacts (identique, pas de SN stockés) |
| **Pause obligatoire** | Seulement après Étape 5 (mal appliquée) | Après chaque Étape 1–5 (systématique) |

---

## 7. Migration vers CIH v3

**Pour S26+** :
- [ ] Utiliser CIH modifié (cih.md mis à jour)
- [ ] Agent affiche résumé synthétique à chaque étape 1–5
- [ ] Utilisateur lit résumé (~2–3 min) + répond optionnellement
- [ ] Agent raffine si feedback
- [ ] Continuité S25 : templates SN ignorés (archivés)

---

## 8. Notes

- **Rétrocompatibilité** : CIH v3 compatible avec tous les rôles cognitifs (PS-ANA-02, PS-SIG-05, etc.) — aucune modification à rôles
- **Protocole Étape 6** : Inchangé (utilisateur décide formellement)
- **Protocole Étapes 7–9** : Inchangé (opérationnalisation)
- **Artefacts AN** : Inchangés, toujours aussi denses et techniques (traceabilité)
