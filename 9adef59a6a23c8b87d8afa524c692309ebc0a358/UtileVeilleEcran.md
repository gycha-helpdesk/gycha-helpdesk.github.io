<!--
Auteur : [Mussa]
Date : [30.09.2025]
Description : Désactiver la veille et l’extinction automatique sur un Mac via Jamf et les réglages système.
-->

# Désactiver la veille et l’extinction automatique sur un Mac

> **Objectif** : Configurer un Mac pour qu’il ne se mette pas en veille et ne s’éteigne pas automatiquement.

---

## 1. Retirer les profils de veille via Jamf

Connectez-vous au dashboard Jamf avec vos identifiants administrateur (**a-xxxxx**) :  
[https://jamf.dgep.edu-vaud.ch:8443/](https://jamf.dgep.edu-vaud.ch:8443/)

```{image} images/jamfRuleDashboard.png
:width: 500px
:name: userveille
:align: center
```

Dans le menu **Profils de configuration**, repérez les trois profils suivants :

- EconomiseurEnergie
- EconomiseurEnergieCo
- ChangeUser

Pour chacun de ces profils, ajoutez l’ordinateur cible dans le champ **Exclusion**.

```{image} images/userveille1.png
:width: 500px
:name: userveille
:align: center
```

---

## 2. Régler le temps d’écran sur « Jamais »

Sur le Mac, ouvrez les **Réglages Système** puis allez dans **Écran verrouillé**.  
Réglez le temps d’écran sur **Jamais**.

```{image} images/userveille2.png
:width: 500px
:name: userveille
:align: center
```

---

## 3. Désactiver la fermeture automatique de session

Toujours dans les **Réglages Système**, rendez-vous dans **Confidentialité et sécurité**.  
Défilez tout en bas et cliquez sur **Avancé**.

```{image} images/userveille3.png
:width: 500px
:name: userveille
:align: center
```

Décochez l’option **Fermer automatiquement la session en cas d’inactivité**.

```{image} images/userveille4.png
:width: 500px
:name: userveille
:align: center
```

---

## 4. Vérifier et annuler les arrêts/redémarrages programmés via le terminal

Pour empêcher que le Mac ne s’éteigne ou ne redémarre automatiquement, utilisez le terminal :

1. **Vérifier les arrêts ou redémarrages programmés**  
   Tapez la commande suivante :

    ```bash
    pmset -g sched
    ```

    ```{image} images/userveille5.png
    :width: 500px
    :name: userveille
    :align: center
    ```

2. **Annuler tous les arrêts/redémarrages programmés**  
   Saisissez la commande suivante :

    ```bash
    sudo pmset schedule cancelall
    ```

---

