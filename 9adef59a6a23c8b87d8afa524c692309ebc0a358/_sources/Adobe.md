<!--
Author:		    Joca Bolli
Date:		    11.04.2022
Description:	fonction de base de adobe console et explication.
-->
# Adobe

> Ici je vais vous expliquer comment remmettre les liscence adobe a zéro (vous n'aurez normalement jamais a le faire mais c'est bien de savoir on c'est).
> Je vais vous montrez également comment crée des PKG avec adobe console.
> et d'autre choses.



## Comment rénisialiser les liscence sur adobe console

Pour pouvoir accéder a adobe console (via internet) il faut savoir quel compte utiliser. Pour cela il faut aller sur DGEP passowrd ou l'alternative si il y en a une. Voici le lien pour accéder a DGEP PASSWORD : https://pass.dgep.edu-vaud.ch:9119/

<br/>

```{image} images/WebDgPassword.png
:width: 800px
:name: WebDgPassword
:align: center
```

<br/>

Une fois que vous avez cliquer sur le lien connecter vous. Dans mon cas j'utiliser mon compte admin a-jbolli. Ensuite cliquer sur Connexion.

<br/>

```{image} images/DGpassowrdInterface.png
:width: 800px
:name: DGpassowrdInterface
:align: center
```

<br/>

Une fois que vous êtes connecter, aller dans la barre de recherche et taperz "adobe" ensuite vous aller voir le compte, copier l'adresse puis cliquer sur ce lien : https://adminconsole.adobe.com/

<br/>

```{image} images/adobeConsoleConexion.png
:width: 800px
:name: adobeConsoleConexion
:align: center
```

<br/>

```{image} images/AdobeConnecxionMdp.png
:width: 800px
:name: AdobeConnecxionMdp
:align: center
```

<br/>

Coller l'adresse mail que vous avez copier juste avant puis cliquer sur "Continuer". copier coller le mot de passe et connecter vous.

<br/>

```{image} images/AdobeConsAccueil.png
:width: 800px
:name: AdobeConsAccueil
:align: center
```

<br/>

Une fois connecter rendez-vous sur "pruduits" pour pouvoir ensuite voir tout ce que vous avez accès. Et entre autre pouvoir modifier les licences.

<br/>

```{image} images/AdobePosteUtiliser.png
:width: 800px
:name: AdobePosteUtiliser
:align: center
```

<br/>

Une fois que vous avez réussi a accèder a cette fenêtre cliquer sur les licences par poste (Poste utilisé). Dans mon cas il y en a beaucoup car nous étions entrain de l'installer sur tout les poste des salles d'informatiques du gymnase.

<br/>

```{image} images/AdobeDefault.png
:width: 800px
:name: AdobeDefault
:align: center
```

<br/>

Ensuite cliquer sur "default" pour pouvoir accéder a differents paramètre dont celuil qui nous intersse.

<br/>

```{image} images/adobeParam.png
:width: 800px
:name: adobeParam
:align: center
```

<br/>

```{image} images/AdobeRecupLiscence.png
:width: 800px
:name: AdobeRecupLiscence
:align: center
```

<br/>

Ensuite cliquer sur les trois petit point puis récupérer les licences. ensuite si vous retourner sur produit vous dervriez normalement voir qu'il n'y a plus d'utilisateur (poste utilisé). Et voila vous savez comment récupérer vos licences.

## Adobe Console créer des PKG.

<br/>

```{image} images/adobePack.png
:width: 800px
:name: adobePack
:align: center
```

<br/>

Pour pouvoir rajouter / créer des pkg il faut dans le menu en haut et cliquer sur packs.


<br/>

```{image} images/AdobeLicencesPartagee.png
:width: 800px
:name: AdobeLicencesPartagee
:align: center
```

<br/>

ensuite selectionner licences partagée, parce que c'est pour un groupe de personne. et elle ne son pas "fixe" et cliquer sur suivant

<br/>

```{image} images/adobeConfCreativ.png
:width: 800px
:name: adobeConfCreativ
:align: center
```

<br/>

selectionner la même chose que sur l'image si dessus. Ensuite cliqewur sur suivant.

<br/>

```{image} images/adobeConfLangue.png
:width: 800px
:name: adobeConfLangue
:align: center
```

```{image} images/adobeConfOS.png
:width: 800px
:name: adobeConfOS
:align: center
```

<br/>


sur cette fenêtre il y a plusieur paramètre a changer, tout dabord il faut changer la langue. Ensuite il faut selectionner pour quel OS vous voulez faire les PKG. Une fois que vous avez choisi ce qu'iil vous convient cliquer sur suivant.


<br/>

```{image} images/adobeAddApp.png
:width: 800px
:name: adobeAddApp
:align: center
```

<br/>

c'est ici que vous allez définir quel application vous aller mettre dans vpotre pkg, le flèche bleu montre comment tout supprimer ou tout rajouter. les carrer rouge a gauche montre les app que vous pouvez rajouter, le carrer rouge a froite montre les app que vous avez rajouter. Une fois que vous vous êtes dessider cliquer sur suivant.

<br/>

```{image} images/adobeConfig.png
:width: 800px
:name: adobeConfig
:align: center
```

<br/>


sur cette page desselectionner **TOUT**, garder ce qui est selectionner de base. Cliquer ensuite sur suivant

<br/>

```{image} images/adobePKGfin.png
:width: 800px
:name: adobePKGfin
:align: center
```

<br/>

Une fois que vous avez fais toutes ces étapes il sufis de cliquer sur "compiler votre pack" est attendre. Maintenant vous savez comment faire ;).

## Comment donne une licences personnel / mobile 

<br/>

```{image} images/srvGadobeUAC.png
:width: 700px
:name: srvGadobeUAC
:align: center
```

<br/>

Pour commencer il faut aller sur le serveur windows (l'AD). ensuite il faut selectionner (user and computer).

<br/>

```{image} images/srvGadobeGychG.png
:width: 600px
:name: srvGadobeGychG
:align: center
```

<br/>

```{image} images/srvAdobeRecherche.png
:width: 400px
:name: srvAdobeRecherche
:align: center
```
<br/>

Ensuite vous devez selectionner GYCHA > puis Groups. Si vous avez du mal a trouver le group vous pouvez simplement effectuer une recherche et le trouver plus rapidement.

<br/>

```{image} images/srvAdobeGoption.png
:width: 400px
:name: srvAdobeGoption
:align: center
```

<br/>

Une fois que vous avez double cliquer sur le groupe vous pourrez rajouter les personne que vous voulez ou alors supprimer des utilisateurs qui fon parti du groupe.


