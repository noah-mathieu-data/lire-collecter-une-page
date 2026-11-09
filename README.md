# lire-collecter-une-page

Semaine 9 de ma formation Data Analyst à la Wild Code School. Le but ici c'est de récupérer moi-même des données sur un site web au lieu d'attendre qu'on me donne un fichier.

Le site c'est [books.toscrape.com](https://books.toscrape.com) un faux catalogue de livres fait pour s'entraîner. J'ai pris la catégorie Poetry contenant 19 livres et une seule page.

Tout est dans `notebooks/collecte.ipynb` et le résultat est dans `data/poetry.csv`.

## Comment j'ai fait ici

J'ai d'abord lu la page de la catégorie pour avoir le titre, le prix, la note et le lien de chaque livre. Ensuite mon script est allé ouvrir les 19 fiches une par une pour récupérer ce qui n'est pas sur la liste, là le stock exact et le code UPC. Une seconde de pause entre chaque page pour ne pas surcharger le site.

## Les soucis rencontrés puis résolus 

Ma première version marchait… à moitié :

- les prix sortaient en *`Â£51.77`* au lieu de *`£51.77`*. Il y avait un problème d'encodage, ensuite réglé avec une seule ligne
- les notes sortaient en mots (*`Four`*) → en fait la note est cachée dans le nom de la classe et non dans le texte
- les liens ressemblaient à *`../../../olio_984/index.html`* ils étaient impossibles à ouvrir tels quels alors il a fallu que je les complète moi même 

Et un titre comme *Quarter Life Poetry: Poems for the Young, Brok...* m'a fait croire qu'il était coupé. C'était juste pandas qui raccourcissait l'affichage. J'ai vérifié aucun titre tronqué.

## Ce que ça donne

19 livres / 235 exemplaires en stock / un prix moyen de 35,97 £. Le plus cher c'est Slow States of Collapse à 57,31 £. Et la poésie est plutôt bien notée, ici 12 livres sur 19 ont 4 ou 5 étoiles.

## Pour le relancer

```bash
python -m venv .venv
source .venv/Scripts/activate
pip install requests beautifulsoup4 pandas notebook ipykernel
```

Noah Mathieu · [LinkedIn](https://www.linkedin.com/in/noah-mathieu-data)
