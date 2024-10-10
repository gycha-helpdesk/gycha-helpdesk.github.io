<!--
Author:		    Alessio Scordato
Date:		    06.02.2024
Description:	marche à suivre pour renomer un poste
-->

# Renomer un mac

## Changer l’inventaire

Changer l'inventaire dans teams en changant le nom des deux macs, un prendra la nom de l'autre (Celui du stock va prendre le nom de celui qui va être remplacé) et l'autre mac va prendre un nom sytle "GYCHA-a201-xyz" (max 15 caractères) et dans la case à coter du nom, mettez l'ancien nom du mac.
```{image} images/ChangeInventaire.png
:width: 600px
:name: ChangeInventaire
:align: center
```
<br>

## Changer le fichier csv

Dans ```smb://jamfrename.dgep.edu-vaud.ch/CSVRepository/GYCHA```, exécutez le script python nommé "gycham_naming_export.py" pour changer le fichier csv avec les bons noms.
<br>

## Renomer les macs

Exécutez la commande « sudo jamf policy -event binding » sur les Macs<br>
Si il y a  dans Partage -> nom d’hôte local, il y a un 2 après le nom, exécutez la commande « sudo jamf policy -event binding »