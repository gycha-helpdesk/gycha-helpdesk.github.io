# Mise à jour des applications dans Jamf

## Description Jamf

C'est une application utilisée par les administrateurs système pour configurer et automatiser les tâches d'administrations informatique pour les appareils macOS, iOS

## avant de la marche à suivre

vous devez installez la nouvelle version que vous voulez.

si elle est en .pkg c'est cool raoul

si c'est en dmg je vous laisse suivre le tuto juste en bas.

Prenons comme exemple VLC

```{image} images/downloadVLC.png
:width: 500px
:name: VLC
:align: center
```

Vous voila avec un fichier DMG

```{image} images/downloadDMG.png
:width: 500px
:name: downloadDMG
:align: center
```

Rendez vous sur composeur est faites new en haut à gauche.

Bon VLC est déjà installé mais vous avez compris le principe.

```{image} images/CreatPkg.png
:width: 500px
:name: PKG
:align: center
```

Enlever les dossiers en trop on veut que l'as mise a jour.

Cliquez sur "Build as PKG" pour le crée.

```{image} images/buildPkg.png
:width: 500px
:name: Build
:align: center
```

Renomer le avec la convention de nomage de JamfAdmin

> ALL_[nom du package avec sa version].pkg
</br>
> GYCH_[nom du package avec sa version].pkg

```{image} images/vlcRename.png
:width: 500px
:name: Rename
:align: center
```

## Début de la marche à suivre avec Jamf

Aprés, c 'être log, allez dans Règle

```{image} images/regleVLC.png
:width: 500px
:name: Jamf
:align: center
```

aller dans la regle déjà existente et changer l'ancien .pkg par le nouveau.

```{image} images/addNewVersionVlc.png
:width: 500px
:name: addNewVersionVlc
:align: center
```

Pour finir allez dans groupe inteligent de VLC

```{image} images/goupIntelligent.png
:width: 500px
:name: goupIntelligent
:align: center
```

en suite modifier le critère du groupe inteligent avec la nouvelle version de VLC

```{image} images/ModifCritere.png
:width: 500px
:name: ModifCritere
:align: center
```

Félicitation tu sais mettre à jour les applications!!!

