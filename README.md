# Kill.py — outil léger d'automatisation de documentation Python

![Logo Python](assets/python-original.svg)

Kill.py est un petit outil CLI pour générer automatiquement de la documentation HTML pour des modules ou paquets Python en s'appuyant sur pydoc (bibliothèque standard). Il vise la simplicité et la rapidité pour documenter du code local ou importable.

Fonctionnalités principales
- Génération rapide de documentation HTML via pydoc.
- Support des chemins vers fichiers/modules et des modules importables.
- Option pour ouvrir automatiquement la doc dans le navigateur.
- Fichier SVG du logo Python inclus dans assets/python-original.svg.

Installation
1. Clonez le dépôt et placez-vous dedans :
```sh
git clone https://github.com/votre-org/votre-repo.git
cd votre-repo
```
2. (Optionnel) créez et activez un environnement virtuel :
```sh
python -m venv .venv
source .venv/bin/activate   # macOS / Linux
.venv\Scripts\activate      # Windows
```
3. (Optionnel) installez les dépendances listées (pour workflows avancés) :
```sh
pip install -r requirements.txt
```

Utilisation rapide
Générer la documentation HTML pour un module importable :
```sh
python kill.py generate mon_module docs/mon_module.html
```

Générer la documentation à partir d'un fichier ou d'un package local :
```sh
python kill.py generate path/to/mymodule.py docs/mymodule.html
python kill.py generate path/to/mypackage docs/mypackage.html
```

Ouvrir automatiquement le fichier généré :
```sh
python kill.py generate my_module docs/my_module.html --open
```

Utilisation depuis Python (API)
```python
from kill import generate_html

generate_html("my_package", "docs/my_package.html")
```

Structure recommandée du dépôt
- assets/
  - python-original.svg  — logo Python (fournie)
- kill.py                — script CLI / API principal
- docs/usage.md          — guide d'usage avancé (Sphinx, MkDocs)
- requirements.txt       — dépendances recommandées (optionnel)
- LICENSE                — licence (ex. MIT)

Conseils pour documentation avancée
- Pour une documentation multi-pages et plus riche, utilisez Sphinx ou MkDocs (voir docs/usage.md).
- Vous pouvez intégrer Kill.py dans un workflow CI pour générer la doc automatiquement et la publier sur GitHub Pages.

Licence
Par défaut, ajoutez la licence de votre choix (ex. MIT) dans le fichier LICENSE.

Auteur
Fixomi (ou remplacez par votre nom)
