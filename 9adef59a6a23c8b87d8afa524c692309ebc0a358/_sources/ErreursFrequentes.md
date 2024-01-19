# Erreurs fréquentes et leurs solutions
Sur cette page vous trouverez des erreurs que nous avons souvent rencontrés et dont nous n'avons parlé nulle part ailleurs sur le site de la documentation avec leur solution. 

# Imprimante bloquée, qui n'imprime plus
Il faut aller sur le serveur d'impression pge000001 et faire un clic droit sur la bonne imprimante > cancel all jobs et redémarrer le serveur d'impression (clic sur le logo windows et restart), ça peut aider.

# Access point Meraki qui clignote/ne fonctionne plus ou switch qui ne fonctionne plus
Faites bien attention au port qui va de la prise ethernet qui distribue du réseau à l'access point. il se pourrait qu'elle soit réglée sur le mauvais VLAN. le bon vlan est: 32 pour les access point et 1 pour les switch (port trunk), regardez aussi les cables sur les switch car si un cable est branché sur deux ports du switch, il s'agit d'une boucle réseau et il faut débrancher une des deux extrémités.

# Imprimante Epson en B01 feuille qui ne sort pas droite
il faut appuyer sur le bouton avec une icone de feuille a4 au milieu de l'epson pour régler le problème. 

# Que faire si une imprimante n'imprime plus
Regarder sur le serveur d'impression voir si des jobs sont en attente dans la queue d'impression:
si oui, vider la queue d'impression, (redémarrer le serveur d'impression sur microsoft remote desktop),

imprimer une feuille de test et le soucis devrait être réglé.
/! c'est une solution possible, il peut s'agir d'un problème physique aussi!

# Message "ARD Désactivé" sur Apple Remote Desktop, quand on essaie de passer une règle UNIX

Si vous rencontrez ce probléme (voir image ci-dessous:)

```{image} images/ardDesactive.png
:width: 500px
:name: ardDesactive
:align: center
```

Il faut fermer Apple Remote Desktop et le rouvrir, en faisant un clique droit sur l'icone d'Apple Remote Desktop dans le Dock et en cliquant sur Quitter. Pas d'autre solution trouvée pour le moment, mais celle-ci fonctionne. Il faudrait relancer l'application environ toutes les deux éxécutions de règles UNIX/autres requêtes.

```{image} images/ardWorking.png
:width: 500px
:name: ardWorking
:align: center
```

# Problème de droits Apple Remote Desktop
Si un message est affiché disant qu'Apple RemoteDesktop n'a pas les droits, allez sous Partage > Gestion à distance et soyez sûr que les comptes remote et adminl y figurent, et quand c'est bon il faut cliquer sur options et être sur que tout est bien coché. si c'est le cas, décocher et recocher les deux premières coches devrait résoudre le problème.

# Problème de droits osascript (Apple Remote Desktop)

Ce problème peut arriver dés qu'on essaie d'éxécuter une commande UNIX sur un poste élève. pour régler le problème, il faut se connecter en adminl sur le poste en question puis aller jusqu'au bureau. Dés que c'est fait, il faut lancer la commande unix ConnexionExam, qui se sert de "osascript" pour fonctionner, puis il y aura un petit message de confirmation pour ajouter les droits nécessaires qu'il faudra accepter.

# Problème de clé SSH Apple Remote Desktop (GetDesktop)

Pour régler ce problème, il faut refaire correctement les clés et liaisons SSH sur un poste en session examen vers les poste prof en session remote. 

Quand c'est fait, il faut aller à la racine du dossier examen (/Users/examen/.ssh) et copier le dossier .ssh

il faut ensuite copier le dossier vers tous les postes élèves des salles informatique et les redémarrer pour que la commande GetDesktop puisse fonctionner.

# Ecrans en noir et blanc sur Apple Remote Desktop

```{image} images/ardNoirEtBlanc.png
:width: 500px
:name: ardNoirEtBlanc
:align: center
```

Pour régler ce problème, il faut juste aller en haut à droite de l'ordinateur regardé, puis tirer le slider vers la droite pour afficher l'écran en couleur.

```{image} images/ardCouleurs.png
:width: 500px
:name: ardCouleurs
:align: center
```

# Comment copier des fichiers ou dossiers vers tous les postes
Pour copier un/plusieurs fichiers vers des postes, il faut cliquer sur le petit bouton "Copier" au centre de ARD:

```{image} images/ardCopieBouton.png
:width: 500px
:name: ardCopieBtn
:align: center
```

Vous arriverez sur ce menu:

```{image} images/ardCopieMenu.png
:width: 500px
:name: ardCopieBouton
:align: center
```

Ensuite, il faut glisser le fichier que vous aimeriez copier dans la section du haut, là ou se trouve le "dossier sans titre" sur l'image ci-dessus puis appuyer sur le bouton Copier en bas de la fenêtre.

# Redémarrer, éteindre, fermer la session etc. d'ordinateurs avec Remote

Il faut sélectionner les postes à observer, les observer puis aller sous Gestion > ce que vous souhaiteriez faire aux ordinateurs:

```{image} images/ardGestion.png
:width: 500px
:name: ardGestion
:align: center
```

Le temps que les ordinateurs éxécutent la commande, il y aura un point d'exclamation affiché sur leurs écrans depuis Remote.



# Problème de lecteur DVD bloqué

Il peut arriver que le bouton pour éjecter le disque d'un lecteur ne fonctionne pas et donc que le lecteur soit bloqué si vous n'avez pas de trombone sur vous.
Pour régler ce problème, il faut faire un clic droit sur l'icone de disque sur votre bureau et cliquer sur éjecter. 
Le disque sera éjecté et le problème n'arrivera plus.

# Problème disques qui se crééent tout seul sur le bureau
Ce problème peut surgir à cause d'une régle pour mettre à jour l'OS d'un poste. Si le poste est trop ancien et donc qu'il ne peut pas supporter le nouvel OS, des disques vont se créer car c'est la seule étape de la règle que l'ordinateur peut faire.

Il faut donc mettre le poste dans la liste des exclusions de la règle jamf et supprimer les disques manuellement en allant dans "Utilitaire de disques" sur le poste.


# Problème de connexion internet/login (pastille rouge)
Si vous n'arrivez pas à vous connecter à un poste avec des identifiants eduvaud, cela peut venir de:
1. Le poste n'est pas correctement lié à l'AD, il faut donc faire les règles renamecomputerout, enlever le poste de l'AD manuellement et renamecomputerin, puis redémarrer le poste. (tout en adminl)
2. le poste à un mauvais DNS, il faut aller dans les paramètres réseau et l'enlever manuellement.

# Que faire quand une application "ne parvient plus à se lancer", qu'elle est corrompue
Pour commencer, il faudra modifier la règle jamf qui installe l'application s'il y en a une qui existe, puis il faut installer le package le plus récent et le mettre sur jamf admin, la règle... 
Ensuite il faut faire une règle qui la supprime et qui la réinstalle avec le script GYCH_eventSequence, qui va devoir éxécuter dans l'ordre une règle qui va d'abord supprimer l'application, puis une autre règle qui va télécharger le bon pkg et l'installer sur le poste, voir règles jamf fixOpenboard & fixOneDrive comme inspiration.

# Le son ne sort pas sur les hauts parleurs dans les salles de cours

Vérifiez que les hauts parleurs soient bien branchés et que leur volume est bien réglé. (pas à 0)
Ensuite, il faut aller sur le macmini et aller dans Son > choisir la bonne sortie audio (s'il y a un ampli Denon il faut le choisir, etc..)
le problème devrait être réglé. Si ce n'est pas le cas, le problème peut soit venir du cable HDMI output/beamer, soit des hauts parleurs (plus rare)

# Les boutons pour hausser/baisser le bureau prof ne marchent pas

L'alimentation qui passe de derrière les boutons à la multiprise qui se trouve à l'arrière du bureau est probablement mal branchée.

# Réseau sur macmini qui est lent / ne fonctionne pas (connexion session AD)
Le problème peut venir de l'ajout du poste dans l'AD qui n'aurait pas été fait correctement, du coup il faut enlever et remettre l'AD et redémarrer le poste. Si ce n'est pas suffisant, il faut contrôler l'espace disque du poste. Si l'espace disque utilisé correspond à environ la moitié ou plus d'espace total utilisable, il faut faire de la place sur le poste et le problème sera réglé. (oui, ça n'a pas beaucoup de sens, mais c'est une solution)

