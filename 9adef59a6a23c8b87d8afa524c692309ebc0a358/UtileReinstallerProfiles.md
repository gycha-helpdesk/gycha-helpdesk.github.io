
<!--
Author:		    Mussa AL Hussein
Date:		    10.04.2024
Description:    marche a suivre pour reinstaller les profiles de JAMF
-->

# Comment supprimer les profil jamf en cas de problème signature non reconnue

Si jamais vous avez besoin d'installer/de réinstaller jamf a cause d'un problème ou autre, ou même tout simplement de supprimer un profil du poste, voici comment faire:

Avec un peu de chance, vous pourrez simplement cliquer sur le petit "-" en bas du profil pour pouvoir le supprimer. Comme ce n'est généralement pas possible, il va falloir le faire autrement.

```{image} images/profilPasSupprimable.png
:width: 800px
:name: profilPasSupprimable
:align: center
```

Si ce n'est pas possible, il va falloir redémarrer le poste en mode récupération/sans échec (touches CMD + R en allumant l'ordinateur):
on devrait arriver sur ce menu:
```{image} images/MenuRecover.png
:width: 800px
:name: MenuRecover
:align: center
```

Ensuite, dans la barre en haut, il faut aller dans utilitaires > terminal

et enter la commande suivante: 

```shell
csrutil disable
```


cette commande sert à désactiver des protections qui empêcheraient des virus d'agir sur le poste. dans notre cas, nous allons désactiver ces protections le temps de supprimer les profils, puis les réactiver dés que c'est fini.

Quand la commande est entrée, vous pouvez redemarrer le poste normalement.

Dés que vous vous êtes connectés (en adminl), il faut ouvrir un terminal, puis entrer les commandes suivantes dans l'ordre:

```shell
cd /var/db/ConfigurationProfiles
```

```shell
sudo rm -rf *
```

```shell
sudo mkdir Settings
```
```shell
sudo touch Settings/.profilesAreInstalled
```

ces commandes serviront à supprimer les profils à la racine de l'ordinateur. quand tout est fini, il faut redémarrer le mac en mode sans échec une dernière fois (cmd+r) pour réactiver les protections de l’intégrité du système:

```{image} images/MenuRecover.png
:width: 800px
:name: MenuRecover
:align: center
```

utilitaires > terminal
puis entrer la commande suivante: 
```shell
csrutil enable
```

On peut maintenant redémarrer le poste normalement, et si tout s'est bien passé, il ne devrait plus y avoir de profil.
maintenant pour réinstaller jamf, il faudra suivre [les étapes d'enrôlement](/JamfEnroll.md). ce sont exactement les mêmes


# Comment enrôler un post dans Jamf

il y a différent moyen d'enrôler un poste :

1. Cela ce fait automatiquement des le moment de l'installation (configuration du post du tout début)
2. Ou grace a un site web (après configuration)

Dans ce doc, je vous explique la deuxième méthode

## Se connecter à DGEP Enroll 

sur la machine que vous voulez enrôler, ouvrez un navigateur et notez dans l'URL cette adresse

```html
https://aus000021.dgep.edu-vaud.ch:8443/enroll
```

n'oubliez pas le **https**
</br>

```{image} images/adresseURL.png
:width: 500px
:name: URL
:align: center
```

</br>
pour vous identifier:

| Identifiant | Mot de passe |
|   :-----:   |   :-----:    |
|  jamfenroll |DGEPEnroll2019|

Après ne remplissez pas la première ligne et indiquer juste dans quel gymnase vous êtes "GYCHA"

```{image} images/enrollename.png
:width: 500px
:name: Enroll
:align: center
```

</br>
En suite cliquer et télécharger le premier profils

⚠ **Quand le profil est installé revenez sur la page pour installer les autres profiles restants.**

Voilà vous l'avez enrôler.