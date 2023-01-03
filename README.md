# Documentation d'Oblyk

Ce projet est dédié à la rédaction de la documentation de l'application d'Oblyk.

_👉 Si vous cherchez la documentation de l'API, rendez-vous sur [la documentation de l'API]_ 

La documentation d'Oblyk utilise le générateur de site statique [Jekyll] avec le thème [Just the Docs].   
Cet outil permet de rédiger facilement la documentation basée sur des fichiers markdowns et inclus une recherche full text "out of the box".

Consulter la partie ["UI Components"] pour vous familiariser avec les syntaxes markdown pour créer des tableaux, titres, listes, etc. 

Oblyk étant un projet majoritairement développé et utilisé en France et que la documentation est destinée aux utilisateurs finaux : la documentation est rédigée en français.

## Les images

Les captures d'écrans de l'interface d'Oblyk doivent être faite en thème clair.

Les liens vers les images dans les pages de la documentation doivent être en chemin relatif, exemple `![une image](../../assets/images/logo.svg)`

**Dimensions :**  
- pour les capture d'écran d'interface desktop, limiter la largeur de l'image à 1920px
- pour les captures sur mobile, limiter la hauteur à 1080px

**Convention de nommage :**  
Les images doivent être nommées comme suit : `[usage-explicite-de-l-image]_[type-d-interface].[format]`  
exemple : formulaire-de-creation-de-compte_desktop.png

**Emplacement sur le projet :**  
Les images doivent se trouver à la racine du dossier /assets/images.  
Pour favoriser la réutilisation des images, nous ne créons pas (par exemple) de sous-dossier par page de documentation.

**Pour annoter les images :**  
Entourez ou encadrez les éléments en jaune avec la couleur suivante : `#fbd033`

## Les liens

Les liens internes doivent être en chemin relatif, exemple: `[un lien](../../sites-naturels/trouver-un-siste-naturel)`

## Tips

### Les alerts

Les alertes sont des paragraphes <p> mis en évidence par une couleur de fond. 
Vous pouvez afficher 4 types d'alertes : `.info`, `.success`, `.warning` et `.danger`

Pour afficher une alerte, faite précéder votre message de la syntaxe `{: .alert .type-d-alert }`

exemple :

```markdown
{: .alert .danger}
Je suis en message inquiétant
```

## Installer et rédiger la documentation localement

Vous devez avoir installé [Jekyll] et [Bundler] d'installé sur votre machine :

1.  Clonez le projet git `git clone git@github.com:oblyk/app-user-doc.git`.

2.  Aller dans le dossier app-user-doc `cd app-user-doc`

3.  Lancer `bundle install` pour installer les gem nécessaire à la génération de la doc.

4.  Lancer `bundle exec jekyll serve` pour générer les fichiers statique to build your site and preview it at `localhost:4000`.

5.  Aller sur `localhost:4000` pour voir le résultat

Quand vous éditez un fichier du projet, jekyll re-génère le site (dans le dossier `_site`), 
vous avez plus qu'à rafraichir votre page pour constater vos changements.

----

[la documentation de l'API]: https://api.oblyk.org/documentation
[Jekyll]: https://jekyllrb.com/
[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[Bundler]: https://bundler.io
["UI Components"]: https://just-the-docs.github.io/just-the-docs/docs/ui-components
