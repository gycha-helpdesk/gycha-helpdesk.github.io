<!-- 
Author:         NoorAlizadeh
Date:           12-Jan 2022
Description:    Installation Anaconda/Jupyter-Book
GYCH-set_Preferences_userLevel_BigSur.sh
 -->

# Anaconda

> Anaconda est une distribution libre et open source2 des langages de
> programmation Python et R appliqué au développement d'applications 
> dédiées à la science des données et à l'apprentissage automatique 
> (traitement de données à grande échelle, analyse prédictive, calcul scientifique), 
> qui vise à simplifier la gestion des paquets et de déploiement3. Les versions de 
> paquetages sont gérées par le système de gestion de paquets conda4. [^1]
> (Source: Wikipdeia)

## Introduction

Dans ce stage/projet pour documenter les differents activié informatique du gymnase, 
nous utilison le package Jupyter-Book qui converti les pages Markdown (.md) dans les
quelles on travail en format Html qui sera enresgistré et publié via Github.

## Installation Jupyter-Book

Logiquement nous allons besoin d'installler [Anaconda][1] d'abord mais il est normalement 
déjà installé sur les postes Gycham. 

Il y a plusieurs maniers d'installer Jupyter-Book, depuis GUI[^2] de 
Anaconda Navigateur ou CLI[^3].

```{note}
Vous aller de toute façon avoir besoin de vos connaissances basiques sur les 
ligne de commandes pour utiliser Jupyter-Book même si on installe le package via la methode GUI.
```

### GUI: Installation Jupyter-Book

Depuis votre machine, ouvrez Anaconda navigateur. Ce nous intéresess est dans la barre de gauche, 
Environments (les environements). 

```{image} images/anaconda-home.png
:width: 600px
:name: anaconda-home
:align: center
```

Quand vous cliquez sur "Environments" vous allez voir tout les environements disponibles, dans 
notre cas il y a seulement le "base" a disposition, nous allons donc créer un autre environement pour
notre package Jupyter-Book.

```{image} images/anaconda-environment.png
:width: 600px
:name: anaconda-envorinments
:align: center
```

Quand vous allez créer un nouvel environment, il vous demande de nommer votre environement et choisir une version de Python. 
Pour le nom nous allons mettre **jupyter-book** et pour la version vous pouvez choisir soit une version antérieur a la 3.8 ou toutes celles d'après.
(j'ai actuellement la 3.10 et elle me semble assez stable).

```{image} images/anaconda-python-version.png
:width: 500px
:name: anaconda-python-version
:align: center
```

Quand l'environement est créé, choisissez le. Ensuite: 

1. Choisissez "not installed" pour afficher les packages qui ne sont pas installés
2. cherchez pour le package "jupyter-book"
3. Selectionnez le package "jupyter-book" dans les resultats
4. Appliques votre choix

```{image} images/anaconda-jupyterbook.png
:width: 600px
:name: anaconda-jupyterbook
:align: center
```

Ensuite appliquez de nouveau les packages montrés dans la fenêtre suivante.


```{image} images/anaconda-jupyterbook-2.png
:width: 500px
:name: anaconda-jupyterbook-2
:align: center
```

Voilà nous avons fini l'installation Jupyter-Book. 

```{image} images/anaconda-jupyterbook-done.png
:width: 600px
:name: anaconda-jupyterbook-done
:align: center
```

Nous pouvons maintenant passer à [Comment Utiliser Jupyter-Book](Utilisation-Jupyterbook) pour builder notre site.

### CLI: Installation Jupyter-Book

L'installation Anaconda sera la même que l'étap précédent. 

1. Pour installer Jupyter-Book ouvrez le terminal de votre machine.
Puis tapez "conda" pour voir si c'est la commande est reconnue. Si l'installation de Anaconda à été correctement fait vous verrez les messages suivant dans le terminal.

```{image} images/anaconda-cli-conda.png
:width: 600px
:name: anaconda-cli-conda
:align: center
```

2. Ensuite nous allons créer l'environment qui contiendra notre package Jupyter-Book. 
La commande pour créer un environment. (nous allons nommer notre environment "jupyter-book"):

```shell
conda create -name jupyter-book
```

```{image} images/anaconda-cli-conda-create-env.png
:width: 600px
:name: anaconda-cli-conda-create-env
:align: center
```

- Qunad le terminal vous demande de continuer avec l'installation ou pas, tapez "y" pour dire yes.
- On peut aussi choisir quelle version python à installer pour cette environment avec la commande suivannte:

```shell
conda create -name jupyter-book python=3.9
```

3. Maintenant on passe à l'installation package jupyter-book dans cet environnement. 
Avant d'installer le package jupyter-book il faut d'abord activer l'environment que nous venons de créer:

```shell
conda activate jupyter-book
```

```{image} images/anaconda-cli-conda-activate-jupyter-book.png
:width: 600px
:name: anaconda-cli-conda-activate-jupyter-book
:align: center
```

Et on voit dans l'image que notre environnement qui était sur (base) est basculer sur jupyter-book.
4. Enfin nous passon à l'installation jupyter-book. 
Le package jupyter-book peut être installer depuis [conda-forge][2], donc si vous voulez faire cette 
installation proprement, suivez en ordre: 

```shell
conda config --add channels conda-forge
```
```shell
conda config --set channel_priority strict
```
```shell
conda install jupyter-book
```

```{image} images/anaconda-cli-conda-forge.png
:width: 600px
:name: anaconda-cli-conda-forge
:align: center
```

Ensuite conda teste les différentes sources pour collecter des packages et les installer. Quand la collecte est fini conda vous demande de valider l'installation, tappez "y" pour valider et normalement c'est tout!

```{image} images/anaconda-cli-conda-jupyterbook.png
:width: 600px
:name: anaconda-cli-conda-jupyterbook
:align: center
```

(Utilisation-Jupyterbook)=
### Utilisation Jupyter-Book

Pour utiliser jupyter-book vous allez utiliser la ligne de commande, c'est comme ça que ça marche, même si vous avez installer jupyter-book avec le GUI de Anaconda.

Jupyter-book suit un schemas pour créer le site, on ne peut pas lancer le build depuis n'importe où. 

```{image} images/build-resources.png
:width: 600px
:name: build-resources
:align: center
```

Dans l'image ci-dessus, on voit le dossier documentation-stage-meta (qui est le dossier qu'on clone depuis Github), les emplacements des fichiers et les sous-dossiers. Le dossier qui nous concerne le plus pour lancer jupyter-book est **src**. Ce dossier contient les documents que vous allez modifiez pour le site et les photos. De coup c'est depuis ce dossier que vous pouvez lancer jupyter-book et créer le site.


En utilisant comand cd[^4] vous pouvez naviguez entre les dossiers. Quand vous êtes bien à l'emplacement dossier source, vous pouvez lancer cette commande: 

```shell
jupyter-book build .
```

```{image} images/build-jupyterbook.gif
:width: 600px
:name: build-jupyterbook
:align: center
```

Quand il a bien généré le site, il vous donne un lien vers le site en local, vous pouvez le copiez dans votre navigateur web pour voir les modifications que vous avez effectué dans vos documentations.

[//]: # (Links)

[1]: https://www.anaconda.com/products/individual#macos
[2]: https://conda-forge.org/

<!-- Refrences dans footer -->

[^1]: <a href="https://fr.wikipedia.org/wiki/Anaconda_(distribution_Python)">Anaconda (Wikipedia)</a>
[^2]: Graphical User Interface, GUI (Interface Graphique)
[^3]: Command Line interface, CLI (Lnterface en Ligne de Commande)
[^4]: cd ou chdir est une commande pour changer la répertoire (<a href="https://fr.wikipedia.org/wiki/Cd_(commande)">Wikipedia</a>)