# Resolution de problème lier au réseau

## Comment régler le problème de Wi-Fi EDUVAUD-INTERNE (solution possible)
### le profil du wifi/réseau
Il faut aller dans les profils de la machine et regarder EDUVAUD-INTERNE. 

```{image} images/Profil-EDU-Interne.png
:width: 300px
:name: favNetwork
:align: center
```

Dedans il faut voire à qui a été disribué (en ouvrant le profil et en scrollant un peu il y a le nom) 

```{image} images/Nom-certificat-EDU-Interne.png
:width: 400px
:name: favNetwork
:align: center
```

et si ce n'est pas la même (que le nom de la machine actuel) il faut mettre la machine dans les exclusions des Profils de configuration JAMF (EDUVAUD-INTERNE) et l'enlever. C'est la même procédure si la machine n'a pas de réseau filaire, le profil est Wired-EDUVAUD-INTERNE et le nom sous les Profils de configuration JAMF (Wired-EDUVAUD-INTERNE)


## Problème de connexion internet/login (pastille rouge) ou Réseau sur macmini qui est lent / ne fonctionne pas (connexion session AD)
Si vous n'arrivez pas à vous connecter à un poste avec des identifiants eduvaud, 
1. vérifier les paramètres réseau (ip = 10.226.40.xxx et le DNS pas 127.0.0.1)

2. Executer la commande
```
sudo jamf policy -event binding
```

Si elle reste bloquer pendant 2-3 min il faut faire un control + C, puis la relancer.

<br>

Si ça ne fonctionne pas il faut:

Enlever le poste de l'AD manuellement dans les paramètres -> Utilisateurs et groupes.
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
il vous demandera 1 ou 2 fois le mot de passe de adminl (remplissez tous les champs).
<br>
Puis lancer la règle sudo jamf policy -event binding. 
<br>
Si ça na toujour pas résolu le problème, il faut Enlever le poste de l'AD manuellement dans les paramètres -> Utilisateurs et groupes. Puis aller dans l'AD et supprimer le poste et refair (sur la machine) sudo jamf policy -event binding.

## Problème compte AD est un compte réseau et pas un compte mobile

Pour savoir si les comptes AD deviennent des compte réseau ou mobile, il faut aller dans les paramètres puis dans utilisateurs et groupes et si vous êtes connecter avec adminl, les compte réseau ne sont pas visible et les comptes mobile oui. les compte réseau on moins de fonctionnalité que les comptes mobile.
<br>
<br>
Pour réparer ce problème il faut aller dans l'utilitaire d'annuaire, déverouiller le cadenas.
```{image} images/ProblemeCompteReseau1.png
:width: 500px
:name: ProblemeCompteReseau1
:align: center
``` 
Puis séléctionner le crayon qui est en bas à gauche. 
```{image} images/ProblemeCompteReseau2.png
:width: 500px
:name: ProblemeCompteReseau2
:align: center
``` 
Sur la nouvelle fenêtre, il faut afficher les options. 
```{image} images/ProblemeCompteReseau3.png
:width: 500px
:name: ProblemeCompteReseau3
:align: center
``` 
Enfin, cocher "crée un compte mobile" et décocher "exiger une confirmation …". 
```{image} images/ProblemeCompteReseau4.png
:width: 500px
:name: ProblemeCompteReseau1
:align: center
``` 