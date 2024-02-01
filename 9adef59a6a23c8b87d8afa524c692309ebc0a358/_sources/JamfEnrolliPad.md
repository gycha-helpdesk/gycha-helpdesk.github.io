
# Comment enroller un Ipad dans Jamf

Si vous avez besoin d'un reset de iPad faites la partie 1, sinon faites la partie 2.

## 1.reset l'iPad
 
on aura besoin de l'application gratuite sur l'app store "apple configuratior 2"

```{image} images/appAppleConfigurator2.png
:width: 500px
:name: AppStore
:align: center
```

l'application sera comme ceci.

```{image} images/ipadNonConnecter.png
:width: 500px
:name: Déconnecter
:align: center
```

Ensuite, brancher l'iPad sur l'ordinateur pour commencer la configuration.
et faites confiance à l'ordinateur ( ipad ).

```{image} images/ConnecterIpad.jpeg
:width: 500px
:name: Cable
:align: center
```

### Début de la manipulation

une fois connecter cliquez sur préparer (barre de menu)

Choisissez une configuration manuelle, cochez "superviser l'appareil" et autoriser le jumelage.

```{image} images/superviserIpad.png
:width: 500px
:name: Superviseur
:align: center
```

Il vous demandera si vous avez un serveur mdm, vous sélectionnez "ne passe s'inscrire... MDM"

```{image} images/nonMDM.png
:width: 500px
:name: ServeurMDM
:align: center
```

Maintenant vous allez créer une organisation pour Chamblandes, si l'organisation est déjà créée vous pouvez la sélectionner.

```{image} images/organisation.png
:width: 500px
:name: Organisation
:align: center
```

Choisissez-les configurations que vous voulez sur votre iPad.

```{image} images/choixconf.png
:width: 500px
:name: ChoixConf
:align: center
```

Voilà il ne reste plus qu'appliquer les paramètres  sur l'iPad.

```{image} images/loadingConf.jpeg
:width: 500px
:name: loadingConf
:align: center
```

## 2. enroller l'iPad

Tout d'abord il faut changer le nom de l'iPad en GYCH_iPad_XX, ça se trouve dans réglages->général->informations->nom.
<br>
Puis, sur le mac dans partage->partage internet,

```{image} images/Share-Connextion1.png
:width: 500px
:name: Share-Connextion1
:align: center
```

configurez le partage pour que votre iPad puisse s'enroller. (P.S. il faut que l'iPad soit bracher sur le mac)

```{image} images/Share-Connextion2.png
:width: 500px
:name: Share-Connextion2
:align: center
```

Sur le mac, téléchargez les profils nécessaire à l'enrollement sans les instaler sur le mac, comme dans "Comment enrôler un post dans Jamf".
<br>
Toujour sur le mac dans "apple configuratior", ajoutez les profils nécessaire à l'enrollement et instalez les dans l'iPad.

```{image} images/Add-profilsMDM-iPad.png
:width: 500px
:name: Add-profilsMDM-iPad
:align: center
```
<br>

À la fin de l'instalation des profils il vous demandera de vous connecter pour pouvoir instaler les applications qui se trouve sur Jamf. Connecter vous dessu avec l'email du helpdesk et sur pass dgep il y aura le mot de passe sous l'onglet "apple store", puis vous receverez un appel avec le code pour la double indentification.