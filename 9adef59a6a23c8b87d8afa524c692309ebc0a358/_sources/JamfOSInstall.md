# Déploiement OS depuis Jamf

## Copy le logiciel

Pour déploiement OSX sur une machine, il nous faut copier le logiciel (pkg) depuis le serveur sur dans le dossier application de la machineen local.
Il y a une règle pour automatiser ce processus dans Jamf.

### Jamf/Règles

Allez sur l'onglet ordinateur de Jamf et ensuite "Règles". Ici vous pouvez faire une recherche pour trouver une règle qui nous aide à copier le package OS depuis le serveur. Si vous ecrivez "copy" dans le champ de recherche il vous affiche les differents packages d'OS. 

```{image} images/copyOS.png

:width: 500px
:name: CopyOSRule"
:align: center
```

<p style="color: 'red'">La version de l'OS (HighSierra, BigSur, etc...) va dependre de la machine sur laquelle vous vous voulez faire cette installe. Pour trouver des infos sur l'OS de la machine vous pouvez maintenant cliquer sur l'icône de pomme au coin de votre monitor et choisir "à propos de ce Mac".</p>

Quand vous êtes sur de la version de l'OS que vous allez installer, vous pouvez selectionner n'import quelle règle et regarder ses configurations.

```{image} images/copyOS.png

:width: 500px
:name: CopyOSRule"
:align: center
```
