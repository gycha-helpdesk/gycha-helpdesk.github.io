<!--
Author:		NoorMohammad Alizadeh
Date:		September 2021
Description:	First steps in using jamf service
-->

# Avant de commencer

## Description Jamf

C'est une application utilisée par les administrateurs système pour configurer et automatiser les tâches d'administration informatique pour les appareils macOS, iOS

## Connexion au Jamf Pro

Pour accéder au Jamf Pro, vous allez passer par son appliance WEB
</br> -> https://10.225.232.161:8443
</br> -> [Jamf Pro Serve Server][2]

### Identification

Jamf Pro vous demande de vous logger avec un compte utilisateur:

```{image} images/login-jamf.png
:width: 300px
:name: log
:align: center
```

</br>

`````{admonition} Identifiant pour un utilisateur JamF Pro
:class: note, dropdown

````{panels}
:column: col-5
:card: border-2
Identifiant
^^^
Gychameta
---
```{dropdown} Mot de passe
Gym_09
```
````
`````

Identifiant pour un super utilisateur Jamf Pro se trouve dans [Password State][1] (DGEP Password) mais vous allez pas avoir besoin de vous connecter au Jamf en tant que superuser.

### Jamf Pro

Après avoir se connecter au Jamf Pro sans erreur. Vous aurez une interface qui resemble à ce que vous voyez dans la capture ci-dessous.

```{image} images/Dashboard-jamf.png
:width: 500px
:name: dashboard
:align: center
```

[//]: # (Links)

[1]: https://pass.dgep.edu-vaud.ch:9119
[2]: https://Aus000021.dgep.edu-vaud.ch


