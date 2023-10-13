<!--
Author:		    Noa Chouriberry
Date:		    03.05.2023
Description:    Inventaire du gymnase (infos)
-->

# Se connecter au serveur de l'inventaire:
Pour voir les fichiers d'inventaire et le script qui nous sera utile, il faut d'abord qu'on se connecte au serveur d'inventaire:

Il faut ouvrir Finder et faire CMD + K à l'intérieur: Vous verrez une fenetre comme ça:
```{image} images/server-window.png
:width: 500px
:name: server-window
:align: center
```

voici l'adresse du serveur a mettre: 
```
smb://gycha-srv-fs01
```

Quand la connexion sera faite, il y aura une fenêtre avec des dossiers à sélectionner. Pour notre part nous allons prendre le dossier IT qui contient les fichiers inventaire:

```{image} images/repertories-window.png
:width: 500px
:name: repertories-window
:align: center
```

# Ou trouver le(s) fichier d'inventaire ?
Dans le finder. On va aller dans inventaire > 2023 (l'année qui correspond, si c'est pour créer un nouveau fichier inventaire il faut créer un dossier avec la nouvelle année) > et le fichier se trouve ici.

# Comment ajouter quelque chose à l'intérieur
En ouvrant le fichier, on se retrouve avec tout ce qui sert à identifier les ordinateurs du gymnase. le type de matériel, la marque, le numéro de serie, le nom...
Pour ajouter du matériel à l'inventaire, il suffit de rajouter une ligne en respectant la mise en forme des autres lignes de l'inventaire et de la modifier par rapport à vos besoins.

```{image} images/fichier-inventaire.png
:width: 500px
:name: fichier-inventaire
:align: center
```