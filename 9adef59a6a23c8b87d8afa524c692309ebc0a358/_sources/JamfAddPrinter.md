# Créer une règle pour ajouter une imprimante dans Jamf



## Avant de débuter 

Il faut ajouter l'imprimante sur le poste, je vous laisse la marche à suivre sur le lien :
https://sites.google.com/view/gycha-it/ressources#h.r65nzqlnc3we

### et

Rajoutez l'imprimante dans Jamf admin si ce n'est pas déja fait .

Sinon allez sur Jamf Admin et cliquez sur "add printer".

```{image} images/addPrintJamfAdmin.png
:width: 500px
:name: JamfAdmin"
:align: center
```

Mettez l'imprimante que vous voulez pour le retrouver dans Jamf.

```{image} images/jamfAdminPrint.png
:width: 500px
:name: addPrint
:align: center
```

Maintenant ouvrez un navigateur et allez sur le Dashboard de Jamf.

```{image} images/Dashboard-jamf.png
:width: 500px
:name: dashboard
:align: center
```

Ensuite dirigez vous sur ordinateur -> Règles

```{image} images/jamfRegle.png
:width: 500px
:name: jamfRegle
:align: center
```

Après vérifier dans les règles déjà existantes s'il y a l'imprimante que vous chercher.

```{image} images/verifierImprimante.png
:width: 500px
:name: verifierImprimante
:align: center
```

Si elle n'est pas la crée une nouvelle règle

Donnez-lui un nom, en cohérence avec l'imprimante que vous voulez (Exemple : Add_Print_b25)

```{image} images/namePrintRegle.png
:width: 500px
:name: namePrintRegle
:align: center
```

Maintenant allez sous imprimantes.

```{image} images/ImprimanteJamf.png
:width: 500px
:name: Imprimante
:align: center
```

Cliquez sur "Configure".

```{image} images/addPrint.png
:width: 500px
:name: addPrint2
:align: center
```

Ajoutez l'imprimante que vous voulez.

```{image} images/addPrintData.png
:width: 500px
:name: Ajouter
:align: center
```

Pour finir allez dans périmètre.

```{image} images/perimetrePrint.png
:width: 500px
:name: Périmètre
:align: center
```

Sélectionez le groupe ou un ordinateur que vous voulez (vous pouvez en choissir plus) .

```{image} images/perimetreAddPrint.png
:width: 500px
:name: Choix
:align: center
```

Il manque plus qu'à appuyer sur "Terminer".

Félicitation vous savez créé une règle pour ajouter une imprimante.

 




