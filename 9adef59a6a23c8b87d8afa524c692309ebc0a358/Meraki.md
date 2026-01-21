<!--
Author:		    NoorMohammad Alizadeh
Date:		    15-nov, 2021
Description:	Meraki web interface login
-->

# Cisco Meraki

> Meraki offre une gestion centralisée des appareils 
> Cisco qui sont facilement accessible depuis un 
> navigateur web ainsi que les telephones portables via 
> Application Meraki. 

````{tabbed} WEB
```{image} images/meraki-web.gif
:width: 450px
:name: meraki-web
:align: left
```
````

````{tabbed} iOS
```{image} images/meraki-appstore.png
:width: 450px
:name: meraki-ios
:align: left
```

:::{link-button} https://apps.apple.com/us/app/meraki/id693056161
:type: url
:text: App Store
:classes: btn btn-outline-primary
:::
````

````{tabbed} Android
```{image} images/meraki-googleplay.png
:width: 450px
:name: meraki-android
:align: left
```

:::{link-button} https://play.google.com/store/apps/details?id=com.meraki.Dashboard&hl=fr_CH&gl=US
:type: url
:text: Google Play Store
:classes: btn btn-outline-success
:::
````

## Login

Pour se connecter à l'interface WEB du Meraki, dabord 
il faut que vous demandiez à votre personne responsable d
e céer un accès à cette interface, ensuite un email avec 
le lien pour créer un mot de passe sera envoyé dans votre 
boîte mail. 

Ensuite, pour acceder au dashboard du Meraki, copiez le 
lien ci-dessous dans votre navigateur WEB:

```
https://meraki.dgep.edu-vaud.ch
```

Ce lien vous amène ver la page login du site Meraki. 
Vous allez simplement tapper votre e-mail via le quel 
votre compte Meraki a été créé, ensuite tappez votre 
mot de passe.

```{image} images/meraki-login-2.png
:width: 500px
:name: meraki-login
:align: center
```

Après avoir saisie l'identifiant et le mot de passe, 
si les informations ont été correctes, vous serez 
dirigez vers le "dashboard" du Meraki, qui va resembler
à la photo ci-dessous.

```{image} images/meraki-dashboard.png
:width: 500px
:name: meraki-dashboard
:align: center
```

## Configuer un port

Sur meraki vous pouvez configurer le port pour un swuitch à distant et le faire marcher via différents VLAN.
Je vous montre comment configurer un port pour avoir accès au réseau imprimantes. 

1. Allez sur le site Meraki et vous logger. Dans le menu à gauche choisissez Switchs. 

```{image} images/meraki-switch.png
:width: 500px
:name: meraki-switch
:align: center
```

2. Dans la list des switch, je choisis SW-A-A19-01 pour notre test.

```{image} images/meraki-switch-a19.png
:width: 500px
:name: meraki-switch-a19
:align: center
```

3. Maintenant on peut choisir quel port on veut configurer. 

```{image} images/meraki-switch-port.png
:width: 500px
:name: meraki-switch-port
:align: center
```

4. Je prends le port 13 comme c'est un port libre. 
   
```{image} images/meraki-switch-port-13.png
:width: 500px
:name: meraki-switch-port-13
:align: center
```

On voit que ce port est configurer avec le VLAN 32 qui est le VLAN management, Trunk.
Cliquez sur l'icône à coté de Configuration pour modifier le port.

5. Danse ces photo vous voyez les modifications nécessaire pour changer le VLAN

````{panels}
**VLAN 32**
^^^
```{image} images/meraki-switch-port-edit.png
:width: 400px
:name: meraki-switch-port-edit
:align: left
```
+++
Avant de changements
---

**VLAN 38**
^^^
```{image} images/meraki-switch-port-edited.png
:width: 400px
:name: meraki-switch-port-edited
:align: right
```
+++
Après les changements
````

Ensuite sauvegardez votre modificaition, l'appareil qui sera connecté à ce port sera dans le VLAN 38, imprimantes.


<!--
Author:		    Joca Bolli
Date:		    24.09.2022
Description:	Information utile et mise a jour du site
-->

## Rajouter un ou plusieurs plan sur meraki 


Connecter vous sur meraki, ensuite aller sur **"Network-wide"** et selcetionner **"Map & Floor plans"**

 <br/>

```{image} images/meraki_mapAndFloor.png
:width: 400px
:name: meraki_mapAndFloor
:align: center
```

<br/>

Vous devrez avoir quelque chose de similaire. Si c'est le cas cliquer sur le bouton bleu **"add a New floor plan"**

 <br/>

```{image} images/Meraki_addNewPlan.png
:width: 800px
:name: Meraki_addNewPlan
:align: center
```
<br/>

Parfais, maintenant il vous faut l'adresse du lieux ou vous voulez poser votre plan, dans mon cas l'adresse du gymnase de Chamblandes, dans le votre certainement aussi. Il suffit de copier l'adresse et de la mettre sur **"location"** juste en dessous du nom qu'aura votre plan. Pour finir séléctionner une image de votre plan et cliquer sur next 


 <br/>

```{image} images/meraki_adressGycha.png
:width: 800px
:name: meraki_adressGycha
:align: center
```

<br/>

```{image} images/Meraki_configPlan.png
:width: 500px
:name: Meraki_configPlan
:align: center
```

<br/>

Une fois que vous avez mis votre plan et que vous l'avez ajuste pour qu'il face la bonne taille et dimension par rapport a l'imeuble de la carte vous pouvez sauvegarder et fermer.

<br/>

```{image} images/Meraki_saveNewPlan.png
:width: 700px
:name: Meraki_saveNewPlan
:align: center
```

<br/>





