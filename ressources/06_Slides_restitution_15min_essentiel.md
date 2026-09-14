# Slides de restitution 15 min — Mini-cours

> Brief associé : M7-B2
> Durée de lecture : ~15 min
> Pré-requis : note de comparaison rédigée

## Pourquoi cette techno ?

Lundi M8, vous présentez **15 min devant la formatrice** (et plus tard un jury en
certif). Une note de 5 pages ne se présente pas telle quelle : il faut des
**slides** qui synthétisent, lisibles **à 3 mètres**. C'est le premier exercice de
restitution orale du parcours — un entraînement direct à la **soutenance M9**
(1 h devant jury).

## Concepts clés

- **Marp** : écrire des slides en Markdown (`---` sépare les slides). Versionnable
  en Git, rendu en PDF/HTML. Alternatives : Slidev, PowerPoint.
- **1 idée par slide** : un titre = un message. Pas de paragraphes.
- **Règle des 3 bullets** : max 3 puces par slide, lisibles à 3 m.
- **Structure 10 slides** : titre+reco / contexte / 3 options (1 chacune) /
  comparatif / recommandation / questions.
- **Le visuel porte** : un schéma vaut un paragraphe (réutiliser les 3 schémas).
- **Répartition en duo** : qui dit quoi (un fait l'audit-reco, l'autre la
  comparaison) — répété avant la restitution.
- **Timing** : 10 min présentation + 5 min Q&A — répéter pour tenir.

## Exemple minimal qui tourne

```markdown
---
marp: true
---
# Évolution du prédicteur — recommandation : Option A
---
## Comparatif
| | A | B | C |
|---|---|---|---|
| Sobriété | ~50€ | ~500€ | ~300€ |
---
## Recommandation : Option A
- 10× moins cher · conformité maîtrisée · gain B/C non démontré
```

## Exercice guidé

1. Construis 10 slides à partir de ta note (1 idée/slide).
2. Vérifie la lisibilité à 3 m (max 3 bullets, gros titres).
3. Avec ton binôme : qui présente quelles slides ? Répétez le timing (10+5).

## Pièges fréquents

| Piège | Conséquence |
|---|---|
| Paragraphes sur les slides | Illisible, on lit au lieu d'écouter |
| > 10 slides | On déborde les 15 min |
| Pas de répartition duo | Restitution décousue |
| Pas de répétition | Dépassement du temps, stress |
| Recommandation noyée | Le message principal se perd |

| Symptôme | Cause probable |
|---|---|
| On dépasse le temps | trop de slides / pas répété |
| Le jury ne retient pas la reco | pas de slide reco claire |
| Slides illisibles au fond | texte trop dense / petit |

## Pour aller plus loin

- Marp : https://marp.app/
- Cf. `slides.md` du correctif (10 slides).

## Vérification (checklist apprenant)

- [ ] ≤ 10 slides, 1 idée par slide.
- [ ] Max 3 bullets/slide, lisible à 3 m.
- [ ] 1 slide **recommandation** claire (+ garde-fou sobriété).
- [ ] Répartition duo définie et répétée.
- [ ] Timing 10+5 tenu en répétition.

> 💡 **Récap** : **1 idée par slide**, ≤ 3 bullets, lisible à 3 m, ≤ 10 slides.
> 1 slide **recommandation** claire + garde-fou sobriété. Répartir la prise de parole
> en duo et **répéter** le timing (10 min + 5 min Q&A). C'est l'entraînement direct à
> la **soutenance M9**.
