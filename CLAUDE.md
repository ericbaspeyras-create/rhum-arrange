# Rhum Arrangé : consignes pour Claude

## L'appli
- Appli web d'une seule page, sans outil de construction : tout est dans `index.html` (style, données, code).
- Installable sur téléphone : `manifest.webmanifest`, `sw.js` (mode hors ligne), icônes `icon-*.png` et `logo.svg` (tonneau avec un pirate).
- Mise en ligne automatique par Netlify (projet `rhum-arrange`) à chaque envoi sur la branche `main`. Adresse : https://rhum-arrange.netlify.app

## Organisation de `index.html`
- `ING` : la liste des parfums (famille, quantité pour 1 L, temps de bain-marie, semaines de macération, préparation…).
- `FORME` : sous quelle forme mettre chaque parfum et ses variantes.
- `SAISON` : mois où chaque fruit est de saison en France.
- `YIELD` : part du fruit qui reste une fois préparé (sert au poids à acheter).
- `FM` (accords entre familles) et `OV` (accords précis entre deux parfums) : `v` vert, `o` orange, `r` rouge. Les lignes `ov(...)` doivent rester après la déclaration de `OV`.
- `COL` (couleur) et `SHAPE` (dessin) pour chaque parfum ; les dessins sont dans la fonction `icon()`.
- Pages : 1 bouteille (volume, degré, bouton Parfums), 2 parfums, 3 méthode et sucre, puis la grande bouteille finale et 4 la recette.

## Règles à respecter
- Tout en français, sans anglicismes, avec des unités françaises (c. à café, c. à soupe, g, cl). Jamais tsp ou tbsp.
- Garder le style pirate (parchemin, rouge corsaire, polices Pirata One et Alegreya, perroquet, sabres, tonneaux).
- Garder l'écran « 18 ans ou plus » et la mention « L'abus d'alcool est dangereux pour la santé. À consommer avec modération. »
- L'eau s'ajoute après filtrage, jamais dans la macération.
- À chaque modification, augmenter le numéro de version du cache dans `sw.js` (`const C="rhum-vN"`), sinon les téléphones gardent l'ancienne version.
- Le propriétaire utilise surtout un téléphone Android : textes courts, gros boutons, présentation verticale.
