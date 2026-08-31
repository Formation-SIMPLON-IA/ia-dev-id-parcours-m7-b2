# M7-B2 — Comparer 3 évolutions architecturales (MediVox)

> **Repo template.** Binôme par affinité technique. « Use this template » →
> `M7-B2-medivox-evolutions-<binome>`. **Pas de code** — conception et arbitrage.
> Restitution orale **en ouverture de M8** (15 min, slides).

---

## 🧭 Votre brief en un coup d'œil

| Support | Rôle |
|---|---|
| **Simplonline** | Le contrat : contexte, livrables, critères |
| **Ce README** | Le pilotage : quoi produire, avec quel mini-cours |
| [`ressources/`](./ressources/) | 7 mini-cours (index dans [`ressources/README.md`](./ressources/README.md)) |
| **Discord `fil-M7-B2`** | Questions communes |

### L'async binôme (jeudi + vendredi matin, 6 h)

| Étape | À produire | Fichier | Appui |
|---|---|---|---|
| 1 | 3 schémas Mermaid (convention cohérente) | `schemas/option_{a,b,c}_TEMPLATE.md` | `01`, `02`, `03` |
| 2 | Comparatif 3×4 **chiffré** | `comparatif_TEMPLATE.md` | `04` |
| 3 | Fallback strategies par option | (dans la note) | `05` |
| 4 | Note 5-8 pages + **recommandation UNE** | `note_comparaison_TEMPLATE.md` | `01`, `05` |
| 5 | Slides 10 max (15 min) | `slides_TEMPLATE.md` | `06` |

Renommez les `*_TEMPLATE` en versions finales.

> ⚠️ La restitution a lieu **en ouverture de M8**, pas cette semaine :
> figez slides + note **vendredi** — dans 10 jours vous ne saurez plus
> pourquoi vous aviez écarté l'option C. Le journal de bord est votre
> assurance-mémoire.

### ✅ Checklist livrables (avant vendredi 17h)

- [ ] 3 schémas **comparables** (mêmes formes/couleurs)
- [ ] Comparatif 3×4 **chiffré** (ordres de grandeur honnêtes, pas « cher »)
- [ ] **Fallback strategies** explicitées par option (seuil / abstention / HITL)
- [ ] **UNE** recommandation tranchée, argumentée chiffrée
- [ ] **Garde-fou sobriété explicite** : justifiez le choix (ou non) d'une
      approche LLM. *« 5 agents pour prédire une DMS »* = signal négatif
- [ ] Slides lisibles à 3 m (≤ 3 bullets/slide). **Journal de bord** tenu

## ⭐ Extension (non notée, si socle bouclé) — l'option B en vrai

Votre comparatif donne un verdict sur l'option B (LLM + RAG) **sur
papier**. Vérifiez-le : montez un mini-RAG mesuré sur le corpus MediVox
(distribué sur Discord, avec son jeu de 12 questions d'évaluation) —
stack du bonus M3-B1 : `sentence-transformers` + ChromaDB, **sans
LangChain**, stop au retrieval. Mesurez **hit@3**, fixez un **seuil
d'abstention** et testez-le sur les 2 questions pièges. Puis répondez
dans votre note : la mesure **confirme-t-elle ou corrige-t-elle** votre
ligne « performance » du comparatif ? Un arbitrage qui survit à un
prototype vaut plus cher qu'un arbitrage de lecture.

## 📚 Ressources

Voir [`./ressources/`](./ressources/) — 7 mini-cours (dont fine-tuning ⭐) + `liens_officiels.md`.

## 🖨️ Rendu slides (optionnel)

`npx @marp-team/marp-cli slides.md -o slides.pdf` ou extension VS Code Marp.
