<!--
Author:		    Mussa AL Hussein
Date:		    24.01.2025
Description:	Information utile et création d'utilisateurs pour le Wifi-Guest
-->
# Wifi EDUVAUD-Guest

>Dans cette documentation, je vais vous expliquer comment créer un utilisateur pour accéder au Wi-Fi EDUVAUD-Guest.


## Comment créer un utilisateur pour le Wifi-guest

Par défaut, la création d’un utilisateur pour le Wi-Fi EDUVAUD-Guest peut sembler compliquée. Voici une méthode simple pour créer un compte et permettre l’accès au réseau :

1 - Ouvrir le navigateur privé 
1. Rendez-vous sur le site Cisco meraki : https://n1.meraki.com/login/dashboard_login/eduvaud?eid=yuBO8b&sso=true
Tappez votre :
loging : pxxyxxx@eduvaud.ch

2. Ajouter un nouvel accès  
Aller dans le menu Meraki en haut à gauche sélectionner Netword-wide/Clients/Users  
```{image} images/Wifi-Guest1.png
:width: 700px
:name: OptionSconfig
:align: center
```
<br/>

3. Cliquer sur Add new user à droit de l’écran
```{image} images/Wifi-Guest2.png
:width: 700px
:name: OptionSconfig
:align: center
```
<br/>

4. Renseigner les divers champs ci-dessous
```{image} images/Wifi-Guest3.png
:width: 700px
:name: OptionSconfig
:align: center
```
<br/>

a.  Description: Mettre le nom en majuscules et le prénom ou l’entreprise éventuellement  

b.  Email : obligatoirement de mettre l'Email

c.  Password : le bouton GENERATE génère un mot de passe  

d.  Autorized : « yes », sinon aucun accès  

e.  Expires : choisir selon demande initiale 


5. Valider par Create user  
Un e-mail est envoyé à l’adresse saisie avec le mot de passe et les logins de connexion comme celui- ci. La personne recevra ce mail avec le login et mot de passe.  


<br/>

2 – Suppression des accès / réactiver les autorisations  
```{image} images/Wifi-Guest3.png
:width: 700px
:name: OptionSconfig
:align: center
```
<br/>

Pour révoquer les autorisatons :  
a.  Sélectionner le compte à révoquer  
b.  Dans Authorization, sélectionner Revoke Autorisation  


Pour réac9ver les autorisa9ons :  
a.  Sélectionner le compte à réactiver  
b.  Dans Authorization, sélection Authorize Users  
