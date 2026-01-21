<!--
Author:         Noa Chouriberry
Date:           10.01.2024
Description:    Page avec des problèmes et solutions qui concernent PaperCut
-->


# Problèmes et solutions PaperCut
 
Cette page vous sera utile si vous recherchez de l'aide concernant PaperCut.

---

<br/>

# Comment retrouver le code PaperCut d'un élève

Pour commencer, il faut se connecter au serveur papercut (pge000001) depuis Microsoft Remote Desktop:

Ensuite, il faut cliquer sur le logo Windows, aller au dossier PaperCut MF et ouvrir Admin Login:

```{image} images/papercutLogin.png
:width: 800px
:name: papercutLogin
:align: center
```
---
  Ca va vous rediriger vers une page web, il faudra ensuite entrer vos identifiants admin pour vous connecter au panel PaperCut

```{image} images/papercutPanel.png
:width: 800px
:name: papercutPanel
:align: center
```
---
  Après, il faut aller dans Users > cliquer sur "Filter off" (sera surement filter ON) et mettre comme filtre le groupe UUS_GYCHA_Teachers si vous voulez connaître l'identifiant d'un professeur ou le groupe UUS_GYCHA_Students si vous cherchez le code d'un élève, puis appuyer sur Apply Filter.

```{image} images/papercutFilter.png
:width: 800px
:name: papercutFilter
:align: center
```
---
  Après vous aurez la liste des profs/élèves qui sont dans le groupe que vous avez renseigné. il vous suffira de chercher son nom/prénom/identifiant eduvaud dans la barre de recherche.
Dés que vous avez trouvé la personne que vous cherchez, il faut cliquer dessus et vous aurez toutes ses informations:

```{image} images/papercutInfo.png
:width: 800px
:name: papercutInfo
:align: center
```
---
  Maintenant, il faut aller tout en bas de la page et vous aurez une section "Card/Identity numbers", le deuxième nombre à 6 chiffres est l'identifiant PaperCut de l'utilisateur.

```{image} images/papercutCode.png
:width: 800px
:name: papercutCode
:align: center
```

<br/><br/>

# Générer un rapport des impressions PaperCut par utilisateur (profs/élèves)

Si vous voulez générer un rapport comme celui ci:(voir screenshot)

```{image} images/papercutRapport.png
:width: 800px
:name: papercutRapport
:align: center
```
---

  Il faut être connecté à PaperCut, puis aller dans Reports et aller vers User Printing - Summary:
```{image} images/papercutMenuReports.png
:width: 800px
:name: papercutMenuReports
:align: center
```
---
  Ensuite, il faut choisir "ad-hoc" dans le menu déroulant et cliquer sur le petit logo "pdf" pour pouvoir exporter le rapport

```{image} images/papercutAdHoc.png
:width: 800px
:name: papercutAdHoc
:align: center
```
---
  Vous vous trouverez sur cette page: 
```{image} images/papercutUserSummary.png
:width: 800px
:name: papercutUserSummary
:align: center
```
---
Vous pouvez choisir la période sur laquelle imprimer un rapport, définir un groupe d'utilisateurs, le type de job d'impression (copie, photocopie..), définir les imprimantes sur lesquelles avoir des informations.. et le format du rapport (pdf, html ou csv).

Pour exporter le rapport, il faut cliquer sur Run Report en bas de la page.

---
  Vous vous trouverez sur cette page: 
```{image} images/papercutRunReport.png
:width: 800px
:name: papercutRunReport
:align: center
```
<br/>

# Les cartes Papercut

Le code se trouve sur teams dans GychaIT dans le canal Imprimantes - Copieurs -> Fichiers -> PaperCut -> Création de cartes PaperCut. Il faut juste télécharger le dossier puis executer le script python dans le dossier du script.
<br/>
le script va sortir un csv qui ne faut surtout pas toucher et un pdf avec les cartes à imprimmer
```{image} images/papercutCards.png
:width: 400px
:name: papercutCards
:align: center
```
Dans Papercut, il faut se connecter avec son compte administrateur, puis aller sur l'onglet "Cartes". Sur la droite il y a "Action" et il faut sélectionner "Importer de nouvelles cartes".
```{image} images/papercutCards1.png
:width: 400px
:name: papercutCards1
:align: center
```
Ensuite il faut séléctionner le fichier csv, puis télécharger 
```{image} images/papercutCards2.png
:width: 800px
:name: papercutCards2
:align: center
```