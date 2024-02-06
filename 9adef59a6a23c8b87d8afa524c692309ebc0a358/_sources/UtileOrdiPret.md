# Ordinateur de prêt

Pour configurer un ordinateur a prêter il faut commencer en lui [installant](https://support.apple.com/fr-ch/HT211683) l'OS qu'il supporte (Catalina pour 2012 et Big Sur pour 2014). Sur ce site il y a toutes les informations et version. De macOS High Sierra jusqu'à macOS Sonoma. Ensuite il faut vérifier que l'ordinateur n'a pas plusieurs disques. Si c'est le cas il faut aller dans "utilitaire de disques" et supprimer ceux en trop et en garder un seul (chamblandesHD). 
<br/>

```{image} images/DiskUtility.png
:width: 400px
:name: DiskUtility
:align: center
```

<br/>

Ensuite, il faut appliquer les règles de jamf (sudo jamf policy). Il faut vérifier que dans les applications l'ordinateur a bien Outlook, Teams, Word, etc. Une fois que vous avez fait toutes ces étapes il ne reste plus qu'a créer un compte admin (le compte adminl, s'il n'est pas déjà là). Il ne faut pas oublier son compte (un compte utilisateur) et modifier dans le teams le fichier inventaire en classifiant l'ordinateur par rapport a son nom.

# La démarche à suivre pour prêter un poste


