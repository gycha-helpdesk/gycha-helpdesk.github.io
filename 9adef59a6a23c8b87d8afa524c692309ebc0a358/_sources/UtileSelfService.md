

<!--
Auteur : Mussa AL Hussein
Date : 01.09.2025
Description : Ajout d’une application dans Self Service (JAMF)
-->


# Documentation JAMF — Self Service

## Comment ajouter une application dans Self Service ?

Voici les étapes pour rendre une application disponible dans Self Service via JAMF :

---

### 1. Connexion au Dashboard JAMF

Connectez-vous au dashboard : [https://jamf.dgep.edu-vaud.ch:8443/](https://jamf.dgep.edu-vaud.ch:8443/) avec vos identifiants administrateur (**a-xxxxx**).

```{image} images/jamfRuleDashboard.png
:width: 500px
:name: jamfRuleDashboard
:align: center
```

---

### 2. Accéder aux règles

Allez dans le menu : **Ordinateurs > Règles**

```{image} images/jamfRuleButton.png
:width: 500px
:name: jamfRuleButton
:align: center
```

---

### 3. Créer une nouvelle règle

Vous verrez la liste des règles JAMF du gymnase. Cliquez sur **Nouveau**.

```{image} images/jamfNewRule.png
:width: 500px
:name: jamfNewRule
:align: center
```

---

### 4. Configurer la règle

Sur la page de création, vous pouvez :
- Donner un nom à la règle
- Lier un paquet d’application (.pkg)
- Lier un script (voir JAMF Admin)

N’hésitez pas à explorer les différentes options pour découvrir tout ce que vous pouvez faire avec une règle JAMF.

```{image} images/jamfRuleOptions.png
:width: 500px
:name: jamfRuleOptions
:align: center
```

---

### 5. Rendre la règle disponible dans Self Service

Dans l’onglet **Self Service**, cochez la case :  
**Rendre la règle disponible dans Self Service**

```{image} images/selfservice5.png
:width: 500px
:name: selfservice5
:align: center
```

---

### 6. Définir le périmètre

Dans l’onglet **Périmètre**, choisissez les utilisateurs ou groupes qui auront accès à cette application.  
Exemple : salles d’informatique.

```{image} images/selfservice6.png
:width: 500px
:name: selfservice6
:align: center
```

---

## Résultat

L’application sera alors disponible dans Self Service pour les utilisateurs concernés.

---

## Conseils


- Testez l’installation via Self Service sur un poste avant un déploiement large.

