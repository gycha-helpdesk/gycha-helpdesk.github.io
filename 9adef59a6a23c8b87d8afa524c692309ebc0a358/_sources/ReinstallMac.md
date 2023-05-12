<!--
Author:		    Noa Chouriberry
Date:		    10.05.2023
Description:    marche a suivre pour reinstaller l'os d'un mac si besoin
-->

# Marche a suivre pour tout reinstaller sur un poste

Cette marche a suivre sera utile si jamais il y a des problèmes au démarrage du mac (dans 99% des cas c'est a cause d'un manque d'espace disque) ou pour régler des problèmes qui ne sont pas réglables en ouvrant une session.

# Centre de restauration

Pour aller à l'endroit qui nous intéresse, il faut éteindre le mac s'il est allumé puis l'allumer en appuyant sur CMD + R le temps du démarrage. Il faut le faire dés le moment ou on a pressé sur le bouton allumer du poste.


Dés que c'est bon, on devrait arriver sur cette page:


(image)


# Effacer le disque

Pour effacer le disque, il faut aller dans l'utilitaire de disque qui se trouve tout en bas. Ensuite, il faut cliquer sur le disque Chamblandes HD et sur le petit moins en haut à droite de la fenêtre.
Quand c'est fini, la prochaine étape est de recréer une partition avec le même nom, ChamblandesHD et de type AFPS. 

# Reinstaller l'OS

Pour réinstaller l'OS sur le disque que nous avons nettoyé, il faut retourner au menu principal et cliquer sur Installer (le nom de l'os). Il faudra sélectionner le disque et puis attendre l'installation.

# Réinstaller les logiciels
Quand tout est bon, il faudra se connecter en adminl sur le poste et faire un sudo jamf policy. Faites attention à bien vous brancher en ethernet.
