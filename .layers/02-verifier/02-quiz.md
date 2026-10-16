---
title: "Deux quiz"
description: "Une question libre, puis un quiz noté"
objectives:
  - Répondre à un quiz d'une question
  - Valider une section par un quiz noté
---

## Une question, pour soi

Ce quiz ne compte pas dans la progression.

```quiz
prompt: Que fait `mkdir -p atelier/projet/src` si `atelier/` n'existe pas ?
answers:
  - "Il crée atelier/, puis projet/, puis src/"
  - "Il échoue : le parent doit exister"
  - "Il ne crée que src/"
correct: 1
explanation: |
  `-p` crée les dossiers parents manquants, et ne dit rien s'ils existent déjà.
```

## Le quiz noté

Celui-ci valide la section quand toutes les réponses sont justes.

```quiz
title: Les blocs d'un cours
tracksProgress: true
questions:
  - prompt: Quel bloc se lance automatiquement à l'ouverture d'une étape ?
    answers: ["setup", "exec", "verify"]
    correct: 1
    explanation: "`setup` prépare l'étape ; `exec` attend un clic sur ▶."
  - prompt: Lesquels ne valident jamais une section à eux seuls ? (plusieurs réponses)
    answers: ["solution", "hint", "verify", "acknowledge"]
    correct: [1, 2]
    explanation: "Une solution et un indice aident, sans valider ; `verify` et `acknowledge` valident."
```
