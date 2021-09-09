# Active Directory de la DGEP

Tous les comptes Eduvaud des élèves et des professeurs sont dans une Active Directory centralisée. L'accès à l'AD est utile pour rechercher des informations sur le compte de quelqu'un ainsi que pour effectuer des manipulations telles que réinitialiser le mot de passe d'une personne par exemple.
---

## Connexion

Que vous soyez connectés dans le réseau du Gymnase ou pas, la procédure d'accès à l'AD est similaire au début.

Tout d'abord, installez l'application *Microsoft Remote Desktop* (vous pouvez la trouver sur l'App Store).

```{image} images/msrd_appstore_ad.png
:width: 500px
:name: msrd_appstore_ad
:align: center
```

Ensuite, cliquez sur le petit "+" dans la barre d'outils, puis *Add PC*:

```{image} images/add_pc_ad.png
:width: 500px
:name: add_pc_ad
:align: center
```

```{image} images/add_pc_2_ad.png
:width: 500px
:name: add_pc_ad
:align: center
```

Vous devriez voir le formulaire suivant :


```{image} images/formulaire_add_pc_empty_ad.png
:width: 500px
:name: AddPc
:align: center
```

## Dans le réseau du Gymnase

À l'intérieur du réseau du Gymnase, il suffit d'ajouter un nouveau PC paramétré comme suit:

```{image} images/formulaire_add_pc_ad.png
:width: 500px
:name: Addpc
:align: center
```

Pour le premier champ, *PC Name*, mettez l'adresse IP du serveur de la DGEP, *10.226.34.17*.

Pour le deuxième champ, *User Account*, un compte doit être créé pour vous.

Les autres champs peuvent être laissés par défaut.

```{tip}
Je conseille de remplir le champ *Friendly name*, il vous permettra de retrouver l'ordinateur plus simplement plus tard.
```

Cliquez ensuite sur *Add* et vous devriez voir l'ordinateur suivant qui est apparu sur la page principale :

```{image} images/pc_created_ad.png
:width: 500px
:name: PcCree
:align: center
```

Comme vous pouvez le voir, j'ai mis "Server AD" dans le champ *Friendly name* du formulaire.

Finalement, double-cliquez sur le carré et une nouvelle fenêtre devrais s'ouvrir, vous demandant si vous voulez bien vous connecter au serveur :

```{image} images/connect_confirm_ad.png
:width: 500px
:name: Confirmation
:align: center
```

Cliquez sur *Continue*, et vous le serveur de la DGEP devrais s'ouvrir dans une nouvelle fenêtre.

```{note}
Le message vous préviens que le certificat n'a pas pu être vérifié. C'est simplement parce que la DGEP produit elle même ses certificats plutôt que de ses les faire créer par une entreprise externe reconnue, mais ça ne devrais pas poser de problèmes de sécurité.
```

---

## Hors du réseau du Gymnase

Hors du réseau du Gymnase, la procédure est un peu plus complexe.

Tout d'abord, ajoutez un nouvel ordinateur dans *Microsoft Remote Desktop* parametré comme suit :

```{image} images/formulaire_add_pc_farm_ad.png
:width: 500px
:name: formulaire_add_pc_farm_ad
:align: center
```

Avec pour l'adresse de l'ordinateur, *PC name*: rdfarm.dgep.edu-vaud.ch.

L'*User account* est le même que précedemment, il doit être créé pour vous.

Un paramètre supplémentaire doit être rentré, le *Gateway*. Pour ce faire, cliquez sur *Gateway* > *Add Gateway*. Vous devriez voir le formulaire suivant :

```{image} images/formulaire_add_gateway_ad.png
:width: 500px
:name: formulaire_add_gateway_ad
:align: center
```

Dans *Gateway name*, mettez : remote.dgep.edu-vaud.ch.

Mettez le nom que vous voulez dans *Friendly name*, puis votre compte dans *User account*.

Une fois que c'est fait, double-cliquez sur le nouvel ordinateur qui s'est ajouté et vous devriez entrer dans le bureau du serveur Windows.

Recherchez ensuite l'application *Microsoft Remote Connection*:

```{image} images/rdfarm_search.png
:width: 500px
:name: rdfarm_search
:align: center
```

Ouvrez-la, vous devriez arriver sur un formulaire que vous compléterez comme suit :

```{image} images/rdfarm_form.png
:width: 500px
:name: rdfarm_form
:align: center
```

Dans *Computer*, mettez l'ip *10.226.34.17*.

Dans *Username*, mettez *DGEP\\<votre_id>* où <votre_id> est l'identifiant qui a été créé pour vous.

Vous pouvez ensuite sauvegarder sous (Save As) cette configuration sur le bureau :

```{image} images/rdfarm_saveas.png
:width: 500px
:name: rdfarm_saveas
:align: center
```

Il suffit ensuite de double-cliquer sur l'icône ainsi créée pour se connecter à l'Active Directory.

## Rechercher un compte

Tous d'abord il faut rechercher "Active Directory" dans la barre de recherche (en bas à gauche).

Ensuite, Sélectionnez EDU --> si possible allez sous dossier GYCHA 

Double-cliquez sur la loupe pour mener une recherche de compte.
(elle se trouve au-dessus des dossiers dans la barre d'outils prêts du filtre).

```{image} images/recherche_ou.png
:width: 500px
:name: recherche_ou
:align: center
```

Notez le nom, le prénom ou les deux et validez la recherche de compte.

```{image} images/recherche_utilisateur.png
:width: 500px
:name: recherche_utilisateur
:align: center
```

Normalement le compte utilisateur devrait apparaitre. Si cela ne marche pas, essayer d'effectuer la recherche plus loin (Genre : dgep.edu-vaud.ch)
```{image} images/AD_recherche_utilisateur.png
:width: 500px
:name: AD_recherche_utilisateur
:align: center
```

Faite un clic-droit sur un des comptes et sélectionnés "propreties".

```{image} images/propreties.png
:width: 500px
:name: propreties
:align: center
```

Dans "General" vous pouvez voir son email.

```{image} images/propreties-email.png
:width: 500px
:name: propreties-email
:align: center
```

Dans "Account" vous pouvez voir ses identifiants et son email.

```{image} images/propreties-log.png
:width: 500px
:name: propreties-log
:align: center
```

## Réinitialiser le mot de passe d'une personne 

Rendez-vous sur le résultat de la recherche des comptes utilisateurs.

```{image} images/AD_recherche_utilisateur.png
:width: 500px
:name: AD_recherche_utilisateur
:align: center
```
  
Clic-droit sur le nom de l'utilisateur qui est affiché et cliquez sur reset password.

```{image} images/Changer_Pwd.png
:width: 500px
:name: Changer_Pwd
:align: center
```

Mettez-lui comme code : Chamblades2021.

Cochez l'option pour que l'utilisateur aille la possibilité de changer son mot de passe.
Si vous n'avez pas le droit de cocher l'option, c'est que l'utilisateur ne fais pas partie du gymnase

Envoyez un mail de confirmation à la personne.

Voilà maintenant vous savez tout.
