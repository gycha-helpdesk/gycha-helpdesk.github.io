# Information complémentaire

> Dans cette partie du site je vais vous explique comment mettre ajour le site / rajouter du contenu.
> en paralelle je vais vous donnez plein d'information concernant les panes que vous pourrez rencontrez et le fonctionnement du réseau de l^école.
> je vais aussi vous expliquer le fonctionnement de l'usi, la dgnsi, la dgep, la dgo et les outils qui sont a notre dispotition.

## Mettre a jour et modifier le site 


Tout d'abord il faut que vous puissez ouvrire les fichiers sur un logiciel de code (j'utiliser visual studio) ensuite il faut que vous vous rendiez dans le finder,
Dans le dossier "src" du site. c'est dans ce dossier que vous allez soit modifiez des fichier existant soit en rajouter. pour le modifier il suffit d'ouvir un fichier qui existe déjà et de le modifier.

```{note}
Pour faire des capture d'écrant il faut appuyer sur : commande, MAJ, 4
```
<br/>

si vous voulez utilisere des image il fsut les mettre dans le dossier image 

```{image} images/rootImage.png
:width: 600px
:name: rootImage
:align: center
```

<br/>

```{image} images/srcSiteRoot.png
:width: 600px
:name: srcSiteRoot
:align: center
```
<br/>

Pour rajouter une fichier c'est un peut plus compliquer. il faut ouvrire le fichier "_toc.yml" et un fois dedans vous pouvez ajouter une section ou une sous section. Dans tout les cas si vous rajoutez quoique ce soit dans ce fichier il faudra aussi créé un fichier dans le dossier "src" avec le même nom.

<br/>

EX : pour créé cette page j'ai du rajouter dans le fichier "_toc.yml" un file du nom de "InformationComplementaire" donc dans le dossier "src" j'ai du créé un fichier du même nom.

<br/>

```{image} images/dossierSRCEtFichier.png
:width: 600px
:name: dossierSRCEtFichier
:align: center
```

<br/>

```{image} images/ContenuFichierToc.png
:width: 600px
:name: ContenuFichierToc
:align: center
```
<br/>

pour aplliquer votre modification il faut executer dans le terminal une suite de commande. Pour ce faire aller dans la barre en haut quand vous etes sur le fichier que vous voulez modifier puis cliquer sur terminal : <br/>

```{image} images/AccesTerminal.png
:width: 600px
:name: AccesTerminal
:align: center
```
<br/>

Ensuite en bas de votre page il devrais y avoir une nouvelle "fenêtre incruster dans vortre fenêtre".<br/>

```{image} images/TerminalInToFenetre.png
:width: 800px
:name: TerminalInToFenetre
:align: center
```
<br/>

 une fois votre modification faite il faut aller sur le temianl est taper la commande :
```shell
conda activate jupyter-book
```

```{note}
Cette commande doit être tapez uniquement si vous n'etes pas déjà sur l'environnement jupyter-book. dans le terminal c'est marqué entre des parenthèse (base) ou (jupyter-book).
```
ex (ici je suis déjà sur jupyter-book): 

<br/>

```{image} images/TypeBaseOuJupy.png
:width: 400px
:name: TypeBaseOuJupy
:align: center
```
<br/>

```{Attention}
pour que la commande fonctionne il faut que vous soyez dans le bon dossier (celui du site). 
```
<br/>

donc si vous ne savez pas ou vous êtes, taper dans le terminal : 
```shell
    pwd
```
<br/>

 Cela vous indique ou vous vous trouvez. ensuite pour vous placer au bon endroit (si vous n'etez pas au bon endroit) il vous suffit de taper "cd" et de glisser le dossier dans lequel vous voulez vous trouvez dans le terminal.
<br/>

Maintenant que vous êtes dans le bon dossier et que vous êtes sur le bonne environement (jupyter-book) vous pouvez tapez la commande suivante : 
```shell
    Jupyter-book build .
```
<br/>
Voila ! une fois que tout ça est fais vous pouvez voir le changemnt en local mais pas en ligne des modification que vous avez apporté au fichier.

```{note}
il suffit de copier le lien qui vous est fourni quand vous tapez la commande build .
```
<br/>

```{image} images/lienSiteLocal.png
:width: 600px
:name: lienSiteLocal
:align: center
```
<br/>

Si vous voulez pouvoir voir vos modifiction en ligne il faut aller sur gitHub desktop pour push toute les données que vous avez modifier. Mais avant ça il faut selectionner le bon dossier.

<br/>

```{image} images/selectionDuBonDossier.png
:width: 400px
:name: selectionDuBonDossier
:align: center
```

<br/>

Un fois que vous êtes sur le bon dossier il faut faire un commmit a la branche principale.

<br/>

```{image} images/Commit.png
:width: 300px
:name: Commit
:align: center
```

<br/>

une fois que c'est fais il faut cliquer sur push en haut a droite. 

<br/>

```{image} images/push.png
:width: 800px
:name: push
:align: center
```

<br/>

Ensuite vous selectionner le deuxième dossier et vous faite la même chose. Une fois que c'est fais vous aller dans le finder et vous aller sur le dossier "src > build > html" et vous copier l'intégraliter du dossier.

<br/>

```{image} images/rootToCopyHtml.png
:width: 800px
:name: rootToCopyHtml
:align: center
```

<br/>

ensuite vous allez sur le dossier (gycha-helpdesk.github.io) est vous coller le tout dans le dossier 9adef59......

<br/>

```{image} images/rootToColler.png
:width: 700px
:name: rootToColler
:align: center
```

<br/>

si ça ne marche pas du premier coup faite toutes ces actions une deuxième fois. ça dévrais marcher. (c'est parce que il y a des dossier qui dépendent d'autre dossier du coup il faut en générale le faire 2 fois).

<br/>

## commande qui pourrais vous être utile

Pour executer une commande jamf il suffi de connecter n'importe quel ordinateur sur le réseau de l'école par câble est aller dans le terminal. Cette commande sert a activier toutes les règle que n'importe quel ordinateur peut avoir.

<br/>

```{Attention}
Pour que la commande fonctionne correctement il faut l'éxecuter plusieur fois. Parce que il y a beaucoup de règle qui sont éxécuter en même temps est certaine règle dépendent d'autre règle. Du coup il est possible que l'executer une seul fois ne suffise pas.
```
<br/>

```shell
    sudo jamf policy
```
<br/>

si vous voulez apeller un règle précisement :

```shell
    sudo jamf policy -event NomDeLaRegle
```
<br/>

```{Attention}
il ne faut pas tapez exactement le nom de la regle. Il faut tapez l'évenement pérsonalisé de la règle (l'encadré en vert). (en générale c'est le nom de la règle). Pour vérifier si le nom de la règle est celui de son évenement pésronaliser son les même il suffis de cliquer sur la règle.
```

<br/>

```{image} images/eventPersonalise.png
:width: 1000px
:name: eventPersonalise
:align: center
```

## Ordinateur de prêt

Pour configurer un ordinateur a prêter il faut commencer en lui [installant](https://support.apple.com/fr-ch/HT211683) l'os qu'il supporte (catalina pour 2012 et Big Sur pour 2014). Sur ce site il y a toutes les information et version. dDe macOS High Sierra jusqu'a macOS Big Sur. Ensuite il faut vérifier que l'rodinateur na pas plusieur disk. Si c'est le cas il faut aller dans "Disk utily" et suprimer ceux en trop et en garder un seul (chamblandesHD). 
<br/>

```{image} images/DiskUtility.png
:width: 400px
:name: DiskUtility
:align: center
```

<br/>

Puis aplliquer les règles de jamf (sudo jamf policy). Il faut vérifier que dans les application l'ordinateur a bien Outlook, Teams, Word, etc. Une fois que vous avez fais toutes ces étapes il ne reste plus qu'a créé un compte admin (user : adminl et mdp : Gym_09). Il ne faut pas oublier son compte (un compte utilisateur) et modifier dans le teams le fichier invantaire en classifiant l'ordinateur par rapport a son nom.

## Shéma réseau des salles de classe en général

VLAN :

- 34 = serveur.
- 48 - 49 = ordinateur personel.
- 40 = Poste de l'école.
- 38 = Imprimante
- 32 = materiel infra (switch, etc)

<br/>

voici les switch réseau que vous retrouverez dans toutes les salle de classe. 

<br/>

```{note}
Le port 1 est pour internet, le port 2 pour le mac mini (le pc fixe), le port 3 le beamer, le port 8 c'est pour les ordinateur personnel des profs.
```

<br/>

```{image} images/avantSwitchReseau.jpg
:width: 600px
:name: avantSwitchReseau
:align: center
```
<br/>

Comme on peut le voir a l'arrière il n'y a que l'alimentation.

```{image} images/ArierreSwitchReseau.jpg
:width: 600px
:name: ArierreSwitchReseau
:align: center
```
<br/>

```{note}
Normalement a l'avant il y a juste le bouton power et input, le bouton input change quel câble hdmi sera afficher au beamer. Comme on peut le voir sur le in 1 ça sera la wacom donc l'ordinateur fixe (le mac mini). In 2 ordi perso donc l'rodinateur que le prof amène ou les élèves. In 3 c'est pour la caméra qui est dans la salle.
```

<br/>

```{image} images/AvantSwitchHDMI.jpg
:width: 600px
:name: AvantSwitchHDMI
:align: center
```
<br/>

```{note}
Le port HDMI "output" c'est le câble HDMI qui relie le beamer (il sert de sortie pour tout les autre), le in 3 est relier a la caméra, le in 2 a l'rodi perso, et le in 1 au mac mini.
```

<br/>

```{image} images/arriereSwitchHDMI.jpg
:width: 600px
:name: arriereSwitchHDMI
:align: center
```

<br/>

```{note}
Sur le mac mini c'est pas compliqué même si il en donne l'impression. Tout a gauche c'est l'alim du mac mini, ensuite c'est le câble réseau donc internet (sur la phto c'est le câble rouge). Après tout le reste est relier ensemble jusqu'au même câble. Sur ce même câble il y a le câble HDMI du mac mini, un câble usb(il sert a relier les port usb de la wacom au mac mini si il y en a) et pour finir l'alim de la wacom est tout ces câbles son réunis en un seul est il est connecter a la wacom.
```
<br/>

```{image} images/macMIiniArriere.jpg
:width: 600px
:name: macMIiniArriere
:align: center
```

<br/>

```{image} images/MultiCableMacMini.jpg
:width: 600px
:name: MultiCableMacMini
:align: center
```

## Fonction / shéma de l'usi / dgep / dgnsi





## Information supplémentaire

### kahoot

Sur kahoot il est possible de lancer en boucle un quizz. Pour ce faire il faut accéder a la bibliothèque ou son organiser tout vos quizz. ensuite cliquer sur jouer (selectionner le quizz que vous voulez lancer en boucle).

<br/>

```{image} images/kahootBiblioJouer.png
:width: 600px
:name: kahootBiblioJouer
:align: center
```

<br/>

 Ensuite une popup s'affichera avec deux xmode de jeu, choissisez celui de gauche.

<br/>

```{image} images/KahootModeDeJeu.png
:width: 600px
:name: KahootModeDeJeu
:align: center
```

<br/>

Une fois le mode de jeux choisi il faut aller dans les option pour les afficher en selectionner [passet automatiquement les questions](https://support.kahoot.com/hc/fr/articles/115016055107-Options-de-jeu-en-direct#auto_move) des questions. 

<br/>

```{image} images/KahootOptionDeJeu.png
:width: 600px
:name: KahootOptionDeJeu
:align: center
```
### VMware / Vsphere

[Comment ce connecter a Vsphere](https://vcenter.dgep.edu-vaud.ch/ui/#?extensionId=vsphere.core.inventory.serverObjectViewsExtension&objectId=urn:vmomi:VirtualMachine:vm-127617:93734f74-49db-4644-be85-8dab90d13b02&navigator=vsphere.core.viTree.hostsAndClustersView)

<br/>

```{image} images/VsphereConnection.png
:width: 400px
:name: VsphereConnection
:align: center
```

<br/>

Sur Vsphere il y a un notation un peut spécial vous pourrez la retrouver ici :

- DUS = DC (Domain controler)
- NGE = Netwotk (DHCP, NPS, FFSO)
- PGE = Printer (papercut)

<br/>

```{image} images/VsphereInterface.png
:width: 400px
:name: VsphereInterface
:align: center
```

<br/>

### Site de vente / achat et imprimante


L'ancien nom du site de "vente, achat" de matériel pour les établissement post obligatoire s'appelais "le Dol". Maintenant il on changer pour "la place".

```{note}
Les écoles post obligatoire on des rabais immense sur les licences, le materiel etc.. (chez dell ça peut aller jusqu'a du 60% voir plus). Il on des licences office pouvant aller jusqu'a 5.- par personne.
```
<br/>

Pour dépanner les imprimantes en générale c'est parce que la personne a mal tapez son mot de passe du coup il faut réafficher la popup et pour ca il faut soit relancer une impression soit cliquer en bas a gauche de l'écrant ensuite il faut cliquer sur la petite flèches et normalement ça reaffichera la popup.

