<!--
Author:		    Alessio Scordato
Date:		    06.02.2024
Description:	marche à suivre pour renomer un poste
-->

# Renomer un mac

## Changer l’inventaire

Changer l'inventaire dans teams en changant le nom des deux macs, un prendra la nom de l'autre (Celui du stock va prendre le nom de celui qui va être remplacé) et l'autre mac va prendre un nom sytle "GYCHA-a201-mm01" et dans la case à coter du nom, mettez l'ancien nom du mac.
```{image} images/ChangeInventaire.png
:width: 600px
:name: ChangeInventaire
:align: center
```
<br>

## Changer le fichier csv

Dans teams, téléchargez le fichier xlsx de l’inventaire et le mettre dans le dossier avec comme nom l'année actuel à coter du script python qui se trouve dans ```smb://fge000001.dgep.edu-vaud.ch./IT/Inventaire```, puis changez le nom du fichier d’inventaire en « inventaire_chamblandes_(année) », puis vérifier le script pour qu'il cherche dans la bonne année et enfin, exécutez le script python pour changer le fichier csv avec les bons noms.
<br>

## Renomer les macs

Exécutez la commande « renamecomputerout » sur les Macs<br>
Finalement, exécutez la commande « renamecomputerin » sur les Macs qui ont été changés<br>
Si il y a  dans Partage -> nom d’hôte local, il y a un 2 après le nom, exécutez la commande «renamecomputer»