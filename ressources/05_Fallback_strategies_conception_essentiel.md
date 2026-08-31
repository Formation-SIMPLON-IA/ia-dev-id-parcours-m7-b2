# Fallback strategies en conception — Mini-cours

> Brief associé : M7-B2
> Durée de lecture : ~20 min
> Pré-requis : notion de seuil, de confiance modèle

## Pourquoi cette techno ?

Un système IA se trompe parfois. Une bonne **architecture** prévoit **quoi faire
quand le modèle n'est pas sûr** : c'est la **fallback strategy**. La concevoir
**dès l'architecture** (pas en réaction à un incident) est un marqueur de
maturité — et un atout de conformité (AI Act supervision humaine). ⚠️ Ici on
parle de fallback en **conception** (choix d'archi), distinct de la réaction au
**drift** en exploitation (M6).

## Concepts clés

- **Seuil de rejet** : si la probabilité prédite est dans une zone d'incertitude
  (ex. 0.4–0.7), **ne pas décider automatiquement** → router vers un humain.
- **Abstention** : le système répond « je ne sais pas » plutôt que de forcer une
  réponse (utile en RAG : pas de contexte → abstention).
- **Human-in-the-loop (HITL)** : un humain valide/tranche les cas incertains ;
  natif dans une archi multi-agents (agent superviseur).
- **Fallback par option** : chaque architecture a son fallback naturel
  (A : seuil de rejet ; B : abstention RAG ; C : HITL via superviseur).
- **Conformité** : le HITL répond à l'AI Act (supervision humaine) et au RGPD
  art. 22 (décision non purement automatisée).
- **Conception ≠ exploitation** : ici on **choisit** la stratégie ; en M6 on
  **réagit** à une dérive observée.

## Exemple minimal qui tourne

```text
Option A — seuil de rejet :
  if 0.4 <= proba < 0.7:  → revue humaine
  else:                   → décision automatique tracée
```

## Exercice guidé

Pour chacune des 3 options MediVox, propose **un** fallback :
1. Option A (ML) : quel seuil de rejet ?
2. Option B (RAG) : quand s'abstenir ?
3. Option C (agents) : quand le superviseur appelle-t-il un humain ?
Relie chaque fallback à une obligation AI Act/RGPD.

## Pièges fréquents

| Piège | Conséquence |
|---|---|
| Aucun fallback | Décisions automatiques indéfendables (art. 22) |
| Confondre fallback (conception) et drift (M6) | Mauvais cadre |
| Seuil de rejet arbitraire | Non justifiable |
| HITL « théorique » sans procédure | Conformité non prouvée |
| Abstention non prévue en RAG | Hallucinations |

| Symptôme | Cause probable |
|---|---|
| Conformité AI Act contestée | pas de supervision humaine prévue |
| Trop de cas en revue humaine | seuil trop large (coût opérationnel) |

## Pour aller plus loin

- AI Act — supervision humaine : https://artificialintelligenceact.eu/the-act/
- Cf. mémoire interne : fallback (conception) ≠ OOD/drift (exploitation).

## Vérification (checklist apprenant)

- [ ] Chaque option a un fallback explicite (seuil / abstention / HITL).
- [ ] Je relie le fallback à une obligation (AI Act art. 14 / RGPD art. 22).
- [ ] Je distingue fallback (conception) et réaction au drift (M6).
- [ ] Mes seuils sont justifiés, pas arbitraires.
- [ ] Le HITL est décrit comme une **procédure**, pas un vœu.

> 💡 **Récap** : prévoir **dès l'architecture** quoi faire quand le modèle n'est pas
> sûr — seuil de rejet (A), abstention (B), HITL (C) — et relier chaque fallback à une
> obligation (AI Act art. 14 / RGPD art. 22). Fallback en **conception** ≠ réaction au
> **drift** en exploitation (M6).

*Réflexe : un fallback est une **procédure** (qui, quand, comment), pas une intention — sinon il n'existe pas en pratique.*
