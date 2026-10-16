---
title: "Lancer une commande"
description: "Préparation automatique, ▶, vérification et indices"
objectives:
  - Lancer une commande depuis le panneau
  - Vérifier son résultat
---

## Préparer l'atelier

À l'ouverture de cette étape, un script de préparation a créé le dossier `atelier/` (bloc
`setup`, sans rien afficher).

```setup
mkdir -p atelier
```

## Écrire un fichier

▶ lance la commande dans le terminal byte_layers ; 📋 la copie.

```exec
echo "bonjour" > atelier/bonjour.txt && cat atelier/bonjour.txt
```

Puis vérifier :

```verify
f=atelier/bonjour.txt
if [ ! -f "$f" ]; then echo "absent : $f — lancer la commande ci-dessus"; exit 1; fi
echo "trouvé : $f"
```

```hint
La commande se lance avec ▶, dans le terminal qui s'ouvre en bas.
```

```hint
À la main : `echo "bonjour" > atelier/bonjour.txt`, depuis le dossier du cours.
```
