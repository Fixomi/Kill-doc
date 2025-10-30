# doc-tools-python

![Logo](assets/logo.svg)

Un outil léger pour générer de la documentation HTML pour des modules Python, avec exemples, instructions d'installation et options pour étendre la doc avec Sphinx ou MkDocs.

## Fonctionnalités
- Génération rapide de documentation HTML pour un module Python via pydoc (librairie standard).
- Exemple CLI prêt à l'emploi (`example.py`) pour produire des fichiers HTML.
- Conseils d'intégration avec Sphinx ou MkDocs pour une documentation plus riche.
- Logo SVG inclus.

## Installation
Clonez le dépôt puis (optionnel) créez un environnement virtuel :
```sh
git clone https://github.com/your-org/your-repo.git
cd your-repo
python -m venv .venv
source .venv/bin/activate  # macOS / Linux
.venv\Scripts\activate     # Windows
pip install -r requirements.txt
```

Remarque : le script principal utilise la librairie standard (`pydoc`) — aucune dépendance obligatoire. Les dépendances listées dans `requirements.txt` sont recommandées pour des workflows avancés (Sphinx, MkDocs, pdoc).

## Utilisation rapide
Générer la documentation HTML d'un module (exemple `example_module`) :

```sh
python example.py generate example_module docs/example_module.html
```

Exemples :
- Générer la doc d'un fichier local `my_package` :
  python example.py generate path/to/my_package docs/my_package.html
- Ouvrir la page générée dans le navigateur (option --open) :
  python example.py generate my_module docs/my_module.html --open

## Exemple d'utilisation depuis Python
Voici comment appeler la fonction de génération depuis un autre script :

```python
from example import generate_html

generate_html("my_package", "docs/my_package.html")
```

## Documentation avancée (Sphinx / MkDocs)
Pour de la documentation navigable et multi-pages, utilisez Sphinx ou MkDocs.
- Sphinx :
  - `pip install sphinx`
  - `sphinx-quickstart` puis configurez `conf.py` et utilisez `sphinx-apidoc` pour générer la doc API.
- MkDocs :
  - `pip install mkdocs mkdocstrings`
  - Configurez `mkdocs.yml` et ajoutez `mkdocstrings` pour l'API.

Voir `docs/usage.md` pour des commandes et exemples détaillés.

## Structure recommandée du dépôt
- assets/logo.svg — logo utilisé dans le README et la doc.
- example.py — script CLI / API pour générer la doc.
- docs/ — documentation utilisateur supplémentaire.
- requirements.txt — dépendances recommandées.
- LICENSE — licence MIT (exemple).

## Contribution
Contributions bienvenues : issues, PRs, suggestions d'amélioration (support Markdown, templates HTML, intégration CI pour publier docs).

- Ouvrez une issue pour discuter une nouvelle fonctionnalité.
- Proposez une PR pour les corrections ou les ajouts.

## Licence
MIT — voir `LICENSE`.

## Contact
Auteur : Fixomi (ou remplacez par votre nom)
