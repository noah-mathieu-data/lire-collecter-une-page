# lire-collecter-une-page

Ma première collecte de données sur un site web faite pendant la semaine 9 de ma formation Data Analyst à la Wild Code School.

J'ai récupéré les 19 livres de la catégorie "Poetry" du site d'entraînement [books.toscrape.com](https://books.toscrape.com), en deux temps :
- d'abord la page de la catégorie (titre, prix, disponibilité, note, lien) ;
- ensuite la fiche de chaque livre (catégorie, stock exact, code UPC).

## Ce qu'il y a dedans

- `notebooks/collecte.ipynb`  ma fiche technique, le code de la collecte et mes réponses
- `data/poetry.csv`  le résultat, 19 livres et 7 colonnes

## Ce que j'ai trouvé

- 235 livres en stock au total
- un prix moyen de 35,97 £
- 12 livres sur 19 ont 4 ou 5 étoiles

## Pour lancer le projet

```bash
python -m venv .venv
source .venv/Scripts/activate
pip install requests beautifulsoup4 pandas notebook ipykernel
```

## Outils

Python, requests, BeautifulSoup, pandas, Git, GitHub

## Contact

[Mon LinkedIn](https://www.linkedin.com/in/noah-mathieu-data)