# Tuto pour ajouter des règles sur Jamf

## Description Jamf :

C'est une application utilisée par les administrateurs système pour configurer et automatiser les tâches d'administrations informatique pour les appareils macOS, iOS

serveur Jamf pro
Aus000021.dgep.edu-vaud.ch
## Début de la marche à suivre :

Tout d'abord ouvrez un navigateur et notez https://10.225.232.161:8443/ dans l'URL.

| Identifiant | Mot de passe |
|-------------|--------------|
|Gychameta|Gym_09|

```{image} images/loginJamf.png
:width: 500px
:name: log
:align: center
```

Vous voilà sur l'acceuil de jamf, vous pouvez voir le Dashboard.

```{image} images/Dashboard-jamf.png
:width: 500px
:name: Dashboard
:align: center
```

Allez sous ordinateur en haut à gauche et cliquer "Règles".


```{image} images/regle-jamf.png
:width: 500px
:name: règle
:align: center
```

Ensuite, cliquez sur nouveau en haut à droite.

```{image} images/addRegle-jamf.png
:width: 500px
:name: addRègle
:align: center
```


Sous Général donner lui un nom (nom de l'application ou ce que vous voulez).

```{image} images/nomNouvelleRegle-jamf.png
:width: 500px
:name: nomDeLaRegle
:align: center
```
Toujours dans Général descendez et cochez les options indiquées.


```{image} images/generalRegle-jamf.png
:width: 500px
:name: regleBase
:align: center
```

Maintenant allez sous "Paquets" (dans la colonne de gauche).


```{image} images/addPaquet-jamf.png
:width: 500px
:name: addDesPaquets
:align: center
```

Cliquez sur "ajouter" à droite sur le paquet que vous voulez.

```{image} images/choixPaquet-jamf.png
:width: 500px
:name: choixPaquet
:align: center
```


Quelques options suplémentaires comme les mises à jour et le point de distribution.

```{image} images/finPaquet.png
:width: 500px
:name: optionSup
:align: center
```

Ensuite allez sur Maintenance (dans la colonne de gauche)

```{image} images/ConfMaintenance-jamf.png
:width: 500px
:name: maintenance
:align: center
```

Regardez que la première case est cochée (Mettre à jours dans l'inventaire)

```{image} images/maintenanceOption-jamf.png
:width: 500px
:name: optionDeMaintenance
:align: center
```

Si tout est bien configurer passons au "Perimètre" de la règle.
Selectionnez un ordinateur ou un groupe dans ce cas là ça sera un groupe.
Pour l'ajouter cliquez sur "add" à droite du groupe.

```{image} images/perimetreGroupe-jamf.png
:width: 500px
:name: perimetre
:align: center
```

Permet de mettre à disposition la règle pour tout les utilisateurs.

```{image} images/selfService-jamf.png
:width: 500px
:name: SelfService
:align: center
```

Se paramètre permet d'afficher l'état d'avancement de l'implémentation de la règle.

```{image} images/afficheDansDashboard-jamf.png
:width: 500px
:name: dashboard
:align: center
```

Félicitation vous savez créé une règle.

