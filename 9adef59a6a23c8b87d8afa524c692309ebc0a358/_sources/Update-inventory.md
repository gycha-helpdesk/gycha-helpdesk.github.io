# Mettre à jour l'inventaire

Pour bien suivre et prendre une trace de changements au niveau des matériels
informatiuques il faut toujours mettre à jour le fichier inventaire dans qui 
se trouve dans le serveur de fichiers. 

```{note}
Actuellement (décembre 2021), le fichier inventaire le plus à jour est celui qui se trouve dans: </br>
Teams > GychaIT > Files > Inventaire > 2020
```

## Accéder au serveur des fichiers

- Pour commencer, ouvrez le Finder et dans les options Finder, choisissez "Aller" et ensuite "Se connecter au servuer"

```{image} images/inventory-file-server.png
:width: 600px
:name: inventory-file-server
:align: center
```

- Dans la fenêtre suivante tappez l'adresse du serveur du fichier puis connecter. Adresse pour acceder au serveur des fichiers:

:::
smb://gycha-srv-fs01
:::

```{image} images/inventory-address.png
:width: 600px
:name: inventory-address
:align: center
```

- Ensuite il vous demande de vous identifier sur le serveur, mettez votre identifiant AD ou Eduvaud puis connectez vous.
  
```{image} images/inventory-login.png
:width: 600px
:name: inventory-login
:align: center
```

- Si authentification s'est faite sans erreur, une autre fenêtre s'ouvre avec une liste des volumes à disposition. Nous allons evidemment choisir IT.

```{image} images/inventory-login-it.png
:width: 600px
:name: inventory-login-it
:align: center
```

Voilà maintenant vous vous êtes bien connecter au serveur des fichiers et vous avez accès au tout les dossiers et documents inventaire. 

```{image} images/inventory-folder.png
:width: 600px
:name: inventory-folder
:align: center
```

## Changer nom d'un poste

Dans les cas où on veut changer le nom d'un pc ou laptop dans l'inventaire nous devons aussi le changer dans Active Directory.
Cela prendre beacoup de temps si on le fesait à la main. Il existe un script Python qui met à jour AD par rappot aux changements dans le fichier inventaire et crée un fichier CSV dans dossier Readonly (il se trouve dans le dossier racine). Donc si on met à jour ce fichier inventaire et lancer le script, AD sera aussi à jour.

Emplacement du fichier inventaire à mettre à jour (dans serveur des fichiers):
```
/IT/inventaire/2021/InventaireNaming.xlsx
```

## Lancer le script Python

Dans le même dossier se trouve le fichier script. Il s'appelle ```gycham_naming_export.py``` . </br>
Pour lancer ce fichier nous aurons besoin du terminal. Dans terminal tappez python ensuite une espace, epuis glisser le script dans terminal. 

```{image} images/inventory-change-post-name.png
:width: 600px
:name: inventory-change-post-name
:align: center
```

Maintenant il vous seulement tappez sur la touche "Enter" pour lancement script. Quand operation réussit, nous pouvons aller voir le fichier CSV que ce script à généré pour voir si le changement à été effectué sans erreur. 

Emplacement du fichier CSV (dans serveur des fichiers): 

```
/IT/ReadOnly/GYCH_naming.csv
```

Dans ce fichier vous pouvez chercher le pc dont vous venez de changer le nom.
