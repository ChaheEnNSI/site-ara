# Site d'Ara Krikorian — Kirk Publishing

Site en ligne : https://chaheennsi.github.io/site-ara/

Site d'une seule page, sans outil à installer : il suffit de modifier les fichiers puis de les envoyer sur GitHub.

## Contenu du dépôt

| Fichier | Rôle |
|---|---|
| `index.html` | Toute la page : styles, textes, catalogue des livres, panier et formulaires |
| `images/` | Couvertures des livres (`livre-<id>.jpg`, `kirk-*.jpg`) et portrait d'Ara Krikorian |

## Modifications courantes

**Ajouter ou modifier un livre** — dans `index.html`, chercher `var LIVRES = [`. Chaque livre est un bloc `{ id: … }` :
copier un bloc existant, lui donner un `id` qui n'est pas déjà utilisé, placer la couverture dans `images/` et indiquer
ses dimensions en pixels dans `w` (largeur) et `h` (hauteur). `group: 'ara'` range le livre parmi ceux d'Ara Krikorian,
`group: 'autres'` parmi les autres auteurs. `isNew: true` affiche le badge « Nouveauté ».

**Ajouter le téléphone ou l'e-mail de contact** — chercher `TÉLÉPHONE` dans `index.html` : un exemple prêt à l'emploi
est en commentaire, il suffit de le décommenter et d'y mettre les vraies coordonnées.

**Commandes et messages** — ils arrivent par e-mail grâce au service gratuit FormSubmit (adresse dans `var ENVOI`).
La toute première fois, FormSubmit envoie un e-mail d'activation à cette adresse : il faut cliquer sur le lien qu'il
contient, sinon les commandes ne sont pas transmises.

## Publier une modification

```
git add -A
git commit -m "Description de la modification"
git push
```

GitHub Pages met le site à jour en 1 à 3 minutes.

## Reste à fournir

- Téléphone et/ou e-mail de contact à afficher.
- Mentions légales et conditions générales de vente (obligatoires en France pour un site qui vend en ligne).
