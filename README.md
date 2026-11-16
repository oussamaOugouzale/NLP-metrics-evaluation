# NLP Evaluation Metrics — 10 métriques

**Master Data & IA — Evaluation Metrics for Natural Language Tasks**  

## Objectif

Comprendre comment évaluer les résultats de trois tâches de **Natural Language Processing (NLP)** : la génération de résumés (*Summarization*), la réponse aux questions (*Question Answering*) et la génération de texte (*Text Generation*).

Le notebook associe à chaque métrique : une explication courte, du **code commenté**, un exemple et une **interprétation du résultat**. Les expériences utilisent principalement un incident de paiement fictif et un exemple de politique RH.

## Les 10 métriques étudiées

| Tâche NLP | Métriques | Objectif |
| --- | --- | --- |
| **Summarization** | ROUGE, BERTScore, QAFactEval | Mesurer le recouvrement, la proximité sémantique et la fidélité factuelle du résumé. |
| **Question Answering** | Exact Match, Token F1, Faithfulness | Vérifier la correspondance à une réponse de référence et l'appui des réponses sur leurs sources. |
| **Text Generation** | Perplexity, Distinct-2, MAUVE, G-Eval | Étudier la prédiction des tokens, la diversité, la distribution des textes et la qualité selon une grille de critères. |

## Exécution sur Google Colab

1. Ouvrir [Google Colab](https://colab.research.google.com/).
2. Choisir **Importer un notebook** et sélectionner `NLP_Evaluation_10_Metriques_Colab.ipynb`.
3. Cliquer sur **Exécution → Tout exécuter**.

Les cellules principales utilisent **Python**, **NumPy** et **Matplotlib** et ne nécessitent ni GPU ni clé API. Le notebook inclut déjà des sorties et des graphiques consultables sans exécution.

## Ce qui est réellement calculé

Il est important de distinguer les **calculs pédagogiques** de l'exécution complète des méthodes de recherche :

- **Calculs exécutés :** ROUGE-1 rappel avec tokenisation simplifiée, Exact Match, Token F1, ratio de Faithfulness à partir d'annotations manuelles, Perplexity avec probabilités fictives et Distinct-2.
- **Illustrations du principe :** BERTScore (vecteurs synthétiques et similarité cosinus), QAFactEval (questions et réponses fournies), MAUVE (nuages de points simulés), G-Eval (notes fictives). Ces exemples **ne sont pas** des évaluations complètes de ces systèmes.
- **Expériences facultatives :** BERTScore avec un modèle préentraîné, Perplexity avec un modèle de langage et algorithme MAUVE sur des vecteurs synthétiques. Elles nécessitent des téléchargements et sont désactivées par défaut.

## Structure du dépôt

```text
nlp-evaluation-metrics/
├── NLP_Evaluation_10_Metriques_Colab.ipynb
└── README.md
```

## Références

- [ROUGE — Lin (2004)](https://aclanthology.org/W04-1013/)
- [BERTScore — Zhang et al.](https://openreview.net/forum?id=SkeHuCVFDr)
- [QAFactEval — Fabbri et al.](https://aclanthology.org/2022.naacl-main.187/)
- [SQuAD — Exact Match et F1](https://aclanthology.org/D16-1264/)
- [RAGAS — Faithfulness](https://docs.ragas.io/)
- [Distinct-n — Li et al.](https://aclanthology.org/N16-1014/)
- [MAUVE](https://krishnap25.github.io/mauve/)
- [G-Eval](https://aclanthology.org/2023.emnlp-main.153/)

*Projet académique : les données et les scores illustratifs ne sont pas des résultats de benchmark sur des services réels.*
