# Tous les serveurs à ajouter sur Microsoft Remote Desktop

/! Vous devrez vous connecter avec un compte admin dgep pour pouvoir vous connecter aux serveurs!!

```{image} images/RmDesktopServers.png
:width: 500px
:name: RmDesktopServers
:align: center
```

## Rdfarm
Le serveur à ajouter est rdfarm. C est le serveur que vous allez utiliser pour vous connectez au autre serveur.<br>
Voici les information à mettre dans Remote Desktop:<br>
PC Name: rdfarm.dgep.edu-vaud.ch<br>
Gateway: GatewayDGEP : <br>cliquer sur gateway > add gateway > Gateway Name: remote.dgep.edu-vaud.ch<br>

pour arriver au même résultat que sur la capture d'écran:
```{image} images/gatewayDgep.png
:width: 500px
:name: gatewayDgep
:align: center
```

## AD

Dans rdfarm, faites un **win+R** (sur un clavier mac c est command+R) et entrer **dsa.msc**, vous aurez la page pour géré l'AD.

## Autre serveurs

Dans rdfarm, ouvrez l'application **mRemoteNG**, puis faites un nouveau dossier, ensuite faites un model, comme dans la screen.
```{image} images/mRemoteNG.png
:name: mRemoteNG
:align: center
```
Copier le model et changer dans connection->Hostname le nom du serveur.
Voici quelque nom de serveur qui pourrait vous être utile:

Serveurs d'impression: pge000001.dgep.edu-vaud.ch