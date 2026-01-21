
# Créer un profil avec Jamf

Les profils jamf servent a créer un profil utilisable sur les mac du gymnase. Ils peuvent être très utile pour faire des choses que les règles ne vous permettent pas forcément de faire, comme par exemple bloquer des options sur les postes ou forcer des paramètres. Le wifi du gymnase GYCHA-INTERNE est attribué par un profil du même nom.

## Profils

Pour aller dans le menu des profils de configuration, il faut aller sous Ordinateur > Profils de configuration (juste en dessous des règles)    

Ensuite, la création de profil se fait de la même manière que les règles, il faut cliquer sur (+) Nouveau et vous aurez un menu qui vous permettera de configurer votre profil.  

```{image} images/jamfProfilConfig.png
:width: 500px
:name: jamfProfilConfig
:align: center
```
---

Vous pouvez mettre un nom au profil (vous devez), et les réglages possibles touchent très souvent aux paramètres par défaut de MacOS, que vous pouvez choisir de forcer ou de désactiver complètement. Je vous conseille de regarder par vous même les possibilités que vous avez en crééant des profils.  

Pour tout le reste, le principe est le même que les règles(périmètre, exclusion..) sauf que pour savoir que votre profil a bien été déployé, il faudra vous rendre dans Profils sur le mac cible et voir que votre profil a bien été ajouté.



