---
title: "Plusieurs critères"
description: "Trois vérifications dans une section, et la solution"
objectives:
  - Lire le verdict de chaque vérification
  - Utiliser la solution sans valider à sa place
---

## Un petit projet

Créer un dossier `atelier/projet` avec un `README.md` qui contient le mot `byte_layers`, et
un dossier `src/`. Chaque critère a sa propre vérification : on voit lequel manque.

```exec
mkdir -p atelier/projet/src
```

```exec
echo "# Mon projet byte_layers" > atelier/projet/README.md
```

```verify
d=atelier/projet/src
if [ -d "$d" ]; then echo "trouvé : $d"; else echo "absent : $d"; exit 1; fi
```

```verify
f=atelier/projet/README.md
if [ -f "$f" ]; then echo "trouvé : $f"; else echo "absent : $f"; exit 1; fi
```

```verify
f=atelier/projet/README.md
if grep -q "byte_layers" "$f" 2>/dev/null; then echo "le README parle de byte_layers"; else echo "le README ne contient pas « byte_layers »"; exit 1; fi
```

```hint
Les deux commandes ci-dessus suffisent, dans l'ordre.
```

````solution
Les deux commandes, en une fois :

```bash
mkdir -p atelier/projet/src
echo "# Mon projet byte_layers" > atelier/projet/README.md
```

La solution ne valide rien : les trois vérifications restent à lancer.
````
