Author:         Noor Mohammad Alizadeh
Date:           07-dec 2021
Description:    Prevent Jamf automatique logout 

# Fermeture Automatique de la sesssion

Ici au GYCHAM nous avons un profile qui ferme automatiquement 
la session d'un utilisateur après un certain temp pour la 
raison de securité.

Je vous montre où se trouve ce profile parce que vous aurez besoin de le désactiver pour un ordinateur afin de pouvoir faire des tests au dessus.

## Désactiver la fermeture automatique d'un session

1. Vous allez tout d'aborad vous connecter au Jamf
2. Dans le menu, allez dans **"Configuration Profiles"** et cherchez le mot **"ChangeUser"**

```{image} images/Jamf-auto-logout.png
:width: 600px
:name: jamf-auto-logout
:align: center
```

3. **Modifiez** ce profile et ajouter le poste que vous volez dans la liste d'exclusion
4. Ensuite sauvegardez votre modification et choisissez **"Distribute to all"**

```{image} images/Jamf-auto-logout-save.png
:width: 600px
:name: jamf-auto-logout-save
:align: center
```

<!-- End -->