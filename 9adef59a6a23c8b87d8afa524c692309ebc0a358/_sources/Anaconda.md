<!-- 
Author:         NoorAlizadeh
Date:           12-Jan 2022
Description:    Installation Anaconda/Jupyter-Book
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

Logiquement nous allons besoin d'installler [1](Anaconda) d'abord mais il est normalement 
déjà installé sur les postes Gycham et c'est compliqué de l'installer nonplus. 

Il y a plusieurs maniers d'installer Jupyter-Book, depuis GUI[^2] de 
Anaconda Navigateur ou l'interface en CLI[^3].

```{note}
Vous aller de toute façon avoir besoin de vos connaissances basiques sur les 
ligne de commandes pour utiliser Jupyter-Book même si on installe le package via la methode GUI.
```

### GUI: Installation Jupyter-Book

Dans votre machine, ouvrez Anaconda navigateur. Ce nous intéresess est dans la barre de gauche, 
Environments (les environements). 

```{image} images/anaconda-home.png
:width: 600px
:name: anaconda-home
:align: center
```

Quand vous cliquez sur "Environments" vous allez voir toutes les environements disponibles, dans 
notre cas il y a seulement le "base" a disposition, nous allons donc créer un autre envoronment pour
notre package Jupyter-Book.

```{image} images/anaconda-environment.png
:width: 600px
:name: anaconda-envorinments
:align: center
```

Quand vous allez créer un nouveau environment, il vous demande de nommer votre environement et choisir une version Python. 
Pour le nom nous allons mettre **jupyter-book** et pour la version c'est mieux de choisir une version différente de 3.8 
parceque apparemment il y avait un problème avec cette version. Choisissez 3.7 ou une version plus récente que 3.8 
(j'ai 3.10 actuellement et ça me semble assez stable).

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


[//]: # (Links)

[1]: https://www.anaconda.com/products/individual#macos

<!-- Refrences dans footer -->

[^1]: <a href="https://fr.wikipedia.org/wiki/Anaconda_(distribution_Python)">Anaconda (Wikipedia)</a>
[^2]: Graphical User Interface, GUI (Interface Graphique)
[^3]: Command Line interface, CLI (Lnterface en Ligne de Commande)