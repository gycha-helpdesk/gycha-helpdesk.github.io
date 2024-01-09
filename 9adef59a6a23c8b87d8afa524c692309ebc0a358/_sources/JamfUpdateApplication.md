<!-- 
Author:         -
Date:           2020    
Description:    How to update packages in jamf
----------------------------------------------
Edit:           3-Dec 2021, Noor Alizadeh
 -->

# Mise à jour des applications dans Jamf

## Types des packages

Quand vous téléchargez la nouvelle version de votre application/package, son type/format sera en pkg ou DMG.

Si c'est un PKG on est bon et on peut passer à l'étape **[Charger le PKG dans JamfAdmin](jamf-admin)**. 
Si c'est un DMG, nous allons essayer de créer un PKG.

### Création d'un PKG à partir d'un fichier DMG

Prenons comme exemple VLC qui est un DMG.

```{image} images/update-pkg-vlc.png
:width: 500px
:name: VLC-update
:align: center
```

</br>

1. Double cliquez sur ce package et l'installez sur votre système. 
2. Ensuite dans le dossier /Applications vous aurez la nouvelle version du VLC, glissez le dans le paneau gauche du JamfComposer 
3. Cela sera ajouté dans la liste des packages à traiter dans JamfComposer.

```{image} images/jamf-update-vlc.png
:width: 500px
:name: jamf-update-vlc
:align: center
```

</br>

Ensuite nous pouvons aller changer le nom du package pour que il 
aie la même norme de nommage que les autre packages.

> **GYCH_VLC_3.0.16.pkg**
> * **_GYCH_** ou **_ALL_** pour montrer que c'est un packet global (ALL) ou specifique pour un etablissement (GYCH)
> * **_VLC_**: ici vous mettez le nom du package, normalement vous n'avez pas besoin de changer le nom du package
> * **_3.0.16_**: la version du package vient après le nom du package, l'info sur la version du package se trouve dans "à propos" de chaque application

```{image} images/jamf-update-vlc-rename.png
:width: 600px
:name: jamf-update-vlc-rename
:align: center
```
</br>

1. Maintenant on peut passer à créer le package en cliquant sur le "Build as PKG"
2. Choisissez ou vous sauvegardez votre PKG et JamfComposer commence à créer le PKG.

(jamf-admin)=
## Charger le le PKG dans JamfAdmin

Nous avons maintenant un package en format PKG qui est pret à être chargé dans le JamfAdmin. </br>

Pour se connecter sur jamf admin, voici les identifiants:
> URL: https://aus000021.dgep.edu-vaud.ch:8443/ <br/>
> Nom d'utilisateur et mot de passe: Voir DGEP Passwords
Ouvrez le JamfAdmin, et il vous juste suffit de glisser le .PKG dans JamfAdmin.

```{image} images/jamf-update-vlc-jamfadmin.png
:width: 500px
:name: jamf-update-vlc-jamfadmin
:align: center
```
</br>

Après avoir mis le package dans Jamf Admin, sauvegardez les changements et le package sera accessible depuis Jamf pro dans les règles.

### Modification des règles pour le package

Ouvrez le Jamf dans votre navigateur, ensuite aller dans Règles
Chercher le nom du package (VLC dans notre cas), modifiez le et dans "Paquets", effacer l'ancien package et ajouter le nouveau puis sauvegardez.

```{image} images/addNewVersionVlc.png
:width: 500px
:name: addNewVersionVlc
:align: center
```
</br>

Pour finir, aller dans "Groupes intelligents" et chercher le nom de votre package. </br>
Vous allez trouver un group qui un nome commençant par "InstallUpdate_"

```{image} images/goupIntelligent.png
:width: 500px
:name: goupIntelligent
:align: center
```
</br>

Ensuite, tapez la nouvelle version du package dans le champ et sauvegardez.

```{image} images/ModifCritere.png
:width: 500px
:name: ModifCritere
:align: center
```


