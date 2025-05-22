<!--
Author:		    Mussa AL Hussein
Date:		    10.04.2024
Description:    marche a suivre pour reinstaller les profiles de JAMF
-->

# Préparation des CO 

Procédure de Réinitialisation de l'Authentification Multi-Facteurs (MFA)  
et utilisation de la Méthode TAP dans Microsoft Entra ID (Azure AD)

**1.Création d’un utilisateur local via JAMF** **:**

Connectez-vous au dashboard JAMF \(https://10.225.232.161:8443/\) avec vos identifiants admin 

Ensuite sous « Règles » Créer une nouvelle règle.

```{image} images/CO_01.png
:width: 1000px  
:name: CO
:align: center  
```
Ensuite dans Général, Ajoutez un nom d’aUichage et cochez les 2 cases \(Actvé et Check-in récurrent\) 

```{image} images/CO_02.png
:width: 1000px  
:name: CO
:align: center  
```
Puis dans « Comptes locaux » Créer un nouveau compte.

```{image} images/CO_03.png
:width: 1000px  
:name: CO
:align: center  
```
Ensuite dans périmètre, choisissez les ordinateurs cibles. 

```{image} images/CO_04.png
:width: 1000px  
:name: CO
:align: center  
```
---

**Partager le fichier CO.mp3 sur les ordinateurs** **:** 

Tout d’abord, il faut télécharger le fichier « CO\_Fichier.sh » depuis le teams GYCHA dans GychaIT >Examen>Fichiers. 

Ensuite, ouvrez le fichier dans visual studio code. 

Puis, modifiez. Le scripte en fonction de vos besoins. 

Explication Variables : 

ALL\_IP : il faut mettre la fin des adresses IP des ordinateurs cible. 

FILE\_NAME : il faut mettre le nom du fichier qu’on veut transférer. 

```{image} images/CO_05.png
:width: 1000px  
:name: CO
:align: center  
```
Une fois que les modifications sont faites, ouvrez un terminal puis exécutez le scripte. 

```{image} images/CO_06.png
:width: 1000px  
:name: CO
:align: center  
```


---

**1.** **Modifier le mot de passe de l’utilisateur local ** **:**

Connectez-vous au dashboard JAMF \(https://10.225.232.161:8443/\) avec vos identifiants admin 

Ensuite sous « Règles » allez sur la page de la règle puis dans utilisateurs locaux. 

1\) Désactiver l’utilisateur pour FileVault 2 

2\) Appuyez sur le \+ en haut à droite. 

```{image} images/CO_07.png
:width: 1000px  
:name: CO
:align: center  
```
Si vous descendez, vous allez voir un deuxième utilisateur comme ci-dessous. 

Ici, il faut ajouter le nouveau mot de passe. 

```{image} images/CO_08.png
:width: 1000px  
:name: CO
:align: center  
```

Et enfin, sauvegardez votre règle. 

---

