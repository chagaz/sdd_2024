# UE 21.2 EC Science des données
Cours « science des données » à Mines Paris (2024). [![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-sa/4.0/)

__Organisation de ce repo__
* `environment.yml` permet de charger l'environnement conda pour les notebooks via l'interface graphique d'Anaconda ou 
```bash
   conda env create -f environment.yml -n sdd2024
   conda activate sdd2024
```
Notez que cet environnement vous fait utiliser JupyterLab et non pas Jupyter Notebook. JupyterLab est plus moderne et plus agréable d'utilisation (voir [la documentation](https://jupyterlab.readthedocs.io/en/stable/)). En particulier, JupyterLab permet de copier des cellules entre notebooks, et l'[extension "Table of contents"](https://github.com/jupyterlab/jupyterlab-toc/blob/master/toc.gif) qui facilite la navigation dans un notebook y est native.
* `poly/` contient tous les fichiers permettant de compiler le poly. La dernière version compilée à jour s'intitule `sdd_2024_poly.pdf`
* `pc/` contient un répertoire par PC
* `projet/` contient les données et instructions relatives au projet numérique.

__Équipe pédagogique__
* Responsable de cours : Chloé-Agathe Azencott
* Chargé·e·s d'enseignement : Nicolas Desassis, Arthur Imbert, Tristan Lazard, Thibaud Martinez, et Lucia Clarotto.

__Emploi du temps__
* __vendredi 7/06 :__ 
  * __09h00-10h30 :__ amphi 1 — Introduction et statistique descriptive (Chapitres 1 & 2)
  * __10h45-12h15 :__ amphi 2 — Estimation et propriétés d'un estimateur (Chapitre 3, sections 3.1 à 3.4)

* __lundi 10/06 :__
  * __09h00-10h30 :__ amphi 3 — Techniques d'estimation (Chapitre 3, sections 3.5 & 3.6)
  * __10h45-12h15 :__ amphi 4 — PC 1 — Statistique inférentielle (TD)

* __vendredi 14/06 :__
  * __09h00-10h30 :__ amphi 4 — Réduction de dimension (Chapitre 4)
  * __10h45-12h15 :__ PC 2 — Réduction de dimension (TP)

* __lundi 17/06 :__
  * __09h00-10h30 :__ amphi 5 — Introduction à l'apprentissage supervisé (Chapitre 6)
  * __10h45-12h15 :__ Mini-projet numérique (1)

* __vendredi 21/06 :__
  * __09h00-10h30 :__ PC 3 — Pré-traitement & introduction à scikit-learn pour l'apprentissage supervisé
  * __10h45-12h15 :__ amphi 6 — Régularisation (Chapitre 7)

* __lundi 24/06 :__
  * __09h00-10h30 :__ PC 4 — Sélection de modèles (TP)
  * __10h45-12h15 :__ amphi 7 — Modèles linéaires pour la classification (Chapitre 7) 

* __vendredi 28/06 :__
  * __09h00-10h30 :__ PC 5 — Modèles linéaires pour la classification (TD)
  * __10h45-12h15 :__ amphi 8 — Modèles d'apprentissage supervisé non-linéaires (Chapitre 8) 

* __lundi 1/07 :__
  * __09h00-10h30 :__ amphi 9 — Séance d'ouverture
  * __10h45-12h15 :__ Mini-projet numérique (2)

* __vendredi 5/07 9h-12h : examen écrit et rendu de projet numérique.__

__Modalités d'évaluation__
* mini-projet numérique à réaliser en binôme. Deux séances de PC y sont dévouées (le 17/06 et le 1/07). À rendre le 5/07 (30%).
* examen sur table avec documents autorisés le 5/07 (70%).

__Pour contribuer à ce repo__
Ce repo contient un script `pre-commit.sh` qui permet de le nettoyer (supprimer les fichiers auxiliaires de latex, nettoyer les notebooks avec [`nbstripout`](https://pypi.org/project/nbstripout/)).

Il est possible de lancer automatiquement ce script lors d'un `git commit` grâce à un [`hook`](https://githooks.com/). Pour cela, il suffit de le copier dans le fichier `.git/hooks/pre-commit` ou d'utiliser un lien symbolique (pour conserver le contrôle de version) :
```bash
    cd .git/hooks/
    ln -s ../../pre-commit.sh pre-commit
```
