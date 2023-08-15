<!--
Author:		    Noa Chouriberry
Date:		    10.05.2023
Description:    marche a suivre pour reinstaller l'os d'un mac si besoin
-->

# Comment supprimer le(s) profil jamf (et n'importe quel profil)

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
