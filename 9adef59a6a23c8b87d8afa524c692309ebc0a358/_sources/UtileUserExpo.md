Le mot de passe de l'utilisateur Expo se trouver dans DGEP Passe.

Tout d'abord rendez-vous sur Jamf puis connectez-vous avec le compte
a-xxx

  -----------------------------------------------------------------------
  <https://jamf.dgep.edu-vaud.ch:8443/>
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

Ensuite dans la barre à gauche, sélectionnez « Réglges » puis rechercher
« user expo change MDP »

![Une image contenant capture d'écran, texte Le contenu généré par l'IA
peut être incorrect.](./zshrboaeo.png){width="5.9863517060367455in"
height="2.1327034120734907in"}\
\
Une fois que vous êtes dans sur la règle, c'est très simple : Défillez
jusqu'à « Comptes locaux » puis définissez le nouveau mot de passe.\
![Une image contenant texte, capture d'écran Le contenu généré par l'IA
peut être incorrect.](./imasaswsge2.png){width="6.026388888888889in"
height="3.4396653543307085in"}\
\
Ensuite il faut enregistrer la règle, et se rendre dans « Journaux »
![Une image contenant texte, capture d'écran Le contenu généré par l'IA
peut être incorrect.](./imageasasas3.png){width="5.31496062992126in"
height="2.6539654418197727in"}

Puis il faut Flush tous les MacBook pour que la règle se lance sur tous.

![Une image contenant texte, ligne, capture d'écran, nombre Le contenu
généré par l'IA peut être
incorrect.](./imagewad4asw.png){width="5.668278652668416in"
height="2.602334864391951in"}

Enfin, il faut s'assurer que la règle s'est lancée sur tous les
ordinateurs. Il suffit de lancer cette commande sur les MacBook :

Sudo jamf policy -event mdpexpo
