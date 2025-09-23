
<!--
Auteur : Mussa AL Hussein
Date : 23.09.2025
Description : Problème de connexion « Vous ne pouvez pas vous connecter en ce moment » — comment résoudre ce problème ?
-->



# Problème « Vous ne pouvez pas vous connecter au compte utilisateur pour le moment »

> **Symptôme** : Message d’erreur « Vous ne pouvez pas vous connecter au compte utilisateur “John Cina” pour le moment ».

> **Cause fréquente** : L’élève est inscrit dans deux gymnases en même temps dans l’Active Directory (AD).

```{image} images/Userlogin1.png
:width: 800px
:name: Userlogin
:align: center
```

---

## Étapes de résolution

### 1. Connexion en administrateur

Connectez-vous sur la machine avec un compte administrateur.

### 2. Ouvrir l’Utilitaire d’annuaire

Ouvrez « Utilitaire d’annuaire » puis double-cliquez sur « Active Directory ».


```{image} images/Userlogin2.png
:width: 800px
:name: Userlogin
:align: center
```

### 3. Modifier les options AD

Dans la fenêtre des options, décochez l’option :  
**« Utiliser le chemin UNC depuis Active Directory »**

```{image} images/Userlogin3.png
:width: 800px
:name: Userlogin
:align: center
```

---

## Conseils supplémentaires

- Vérifiez que l’élève n’est inscrit que dans un seul gymnase dans l’AD.
- Redémarrez la machine après modification si le problème persiste.

Si le problème n’est pas résolu, contactez le support informatique.
