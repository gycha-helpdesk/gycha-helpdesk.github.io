# Resolution de problème lier au réseau

## Comment régler le problème de Wi-Fi GYCHA-INTERNE (solution possible)

Il peut arriver que le wifi GYCHA-INTERNE se déconnecte et se reconnecte en boucle tout seul, et ça peut être (99% des cas) dû à une mauvaise liaison entre le poste et l'AD.

```{image} images/favNetwork.png
:width: 500px
:name: favNetwork
:align: center
```

Pour régler ce problème, il faut commencer par mettre le poste dans la liste des exclusions du profil jamf GYCHA-INTERNE.

```{image} images/gychaInterneExclusion.png
:width: 500px
:name: gychaInterneExclusion
:align: center
```

Ensuite, il faut ouvrir un terminal et entrer la commande suivante:

```
sudo jamf policy -event renamecomputerout
```

```{image} images/terminalRnComputerOut.png
:width: 500px
:name: terminalRnComputerOut
:align: center
```

Ca permettera de sortir le poste de l'AD. Après il faut aller dans Utilisateurs et Groupes > Options et sous Compte serveur réseau, cliquer sur modifier pour supprimer l'ad DGEP. 
il vous demandera d'entrer l'identifiant adminl 2 fois, puis l'AD sera completement supprimée du poste. 

```{image} images/adDGEPEdit.png
:width: 500px
:name: adDGEPEdit
:align: center
```

Il faut cliquer sur le petit " - " pour supprimer l'AD du poste:


```{image} images/DGEPUserGroupes.png
:width: 500px
:name: DGEPUserGroupes
:align: center
```

```{image} images/loginEnleverAD.png
:width: 500px
:name: loginEnleverAD
:align: center
```

Après il faudra retourner sur le terminal et remettre le poste dans l'AD avec la commande suivante:

```
sudo jamf policy -event renamecomputerin
```

Quand la commande est terminée, il faut redémarrer le poste et se connecter. Après avoir ouvert une session, vous pouvez enlever le poste des exclusions du profil GYCHA-INTERNE et le problème devrait être réglé.

```{image} images/gychaInterneLogged.png
:width: 500px
:name: gychaInterneLogged
:align: center
```

## Problème de connexion internet/login (pastille rouge) ou Réseau sur macmini qui est lent / ne fonctionne pas (connexion session AD)
Si vous n'arrivez pas à vous connecter à un poste avec des identifiants eduvaud, cela peut venir de:
1. Le poste n'est pas correctement lié à l'AD, il faut donc enlever le poste de l'AD manuellement dans les paramètres -> Utilisateurs et groupes.
```{image} images/removeAD1.png
:width: 500px
:name: removeAD1
:align: center
```
```{image} images/removeAD2.png
:width: 500px
:name: removeAD2
:align: center
```
il vous demandera 2 fois le mot de passe de adminl (remplissez tous les champs).
<br>
Puis lancer la règle renamecomputerin, puis redémarrer le poste. (tout en adminl)

2. le poste à un mauvais DNS, il faut aller dans les paramètres réseau et l'enlever manuellement.