
<!--
Author:         Mussa AL Hussein
Date:           01.09.2025
Description:    Ajout application sur Self Service (JAMF)
-->

# Documentation JAMF Self-Service

## Comment ajouter une application dans Self-Service ?

Pour ajouter une application sur Jamf, il faut se connecter au dashboard :  
👉 [https://jamf.dgep.edu-vaud.ch:8443/](https://jamf.dgep.edu-vaud.ch:8443/) avec vos identifiants admin (**a-xxxxx**).


```{image} images/jamfRuleDashboard.png
:width: 500px
:name: jamfRuleDashboard
:align: center
```

---
  Ensuite il faut aller sur Ordinateurs > Règles

```{image} images/jamfRuleButton.png
:width: 500px
:name: jamfRuleButton
:align: center
```
---
  Et la vous verrez toutes les règles jamf du gymnase. Après il faut cliquer sur "Nouveau"

```{image} images/jamfNewRule.png
:width: 500px
:name: jamfNewRule
:align: center
```
---
  Vous arriverez sur cette page: Vous pouvez mettre un nom à la règle, y lier un paquet d'application (.pkg), lier un script (voir jamf admin), etc.. Je vous conseille de fouiller par vous même comme ça vous verrez tout ce que vous pouvez faire avec une règle jamf.

```{image} images/jamfRuleOptions.png
:width: 500px
:name: jamfRuleOptions
:align: center
```
---
## Self Service
  Ensuite dans l’onglet Self-Service, coche la case Rendre la règle disponbile dans Self-Service 

```{image} images/selfservice5.png
:width: 500px
:name: jamfDeclencheurs
:align: center
```
---

  ### Périmètre
Ensuite dans l’onglet « Périmètre » Il faut choisir pour qui vous voulez que cette application soit disponible. 
Dans mon cas, j’ai mis les salles d’informatique : 

```{image} images/selfservice6.png
:width: 500px
:name: jamfDeclencheurs
:align: center
```

Et ensuite votre application sera disponible dans Self- Servie. 