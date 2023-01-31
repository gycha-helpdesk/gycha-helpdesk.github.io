<!--
Author:		    Joca Bolli
Date:		    01.02.2022
Description:	Information utile et mise a jour du site


Edit:           Noa Chouriberry
Date:           26.01.2023
Description:    Mise à jour des informations de la page
-->
# Information complémentaire
>Je m'excuse d'avance pour les fautes d'orthographe.
> Dans cette partie du site je vais vous explique comment mettre à jour le site / rajouter du contenu.
> En parallèle je vais vous donner plusieurs d'informations concernant les pannes que vous pourrez rencontrer et le fonctionnement du réseau de l'école.
> je vais aussi vous expliquer le fonctionnement de l'usi, la dgnsi, la dgep, la dgo et les outils qui sont à notre disposition. Et plein d'autres choses qui pourront vous être utiles.

## Mettre a jour et modifier le site 

Tout d'abord il faut que vous puissiez ouvrir les fichiers sur un logiciel de code (je vous conseille Visual Studio Code pour la suite_) ensuite il faut que vous vous rendiez dans le finder,
Dans le dossier "src" du site, c'est dans ce dossier que vous allez soit modifier des fichiers existant soit en rajouter. pour le modifier il suffit d'ouvrir un fichier qui existe déjà et de le modifier.

```{note}
Pour faire des captures d'écran il faut appuyer sur : cmd, MAJ, 4
```
<br/>

si vous voulez utiliser des images il faut les mettre dans le dossier image 

```{image} images/rootImage.png
:width: 700px
:name: rootImage
:align: center
```
<br/>

Pour rajouter un fichier c'est un peut plus compliqué. Il faut ouvrir le fichier "_toc.yml" et une fois que c'est fait vous pouvez ajouter une section ou une sous-section. Dans tous les cas si vous rajoutez quoique ce soit dans ce fichier il faudra aussi créé un fichier dans le dossier "src" avec le même nom.

<br/>

```{image} images/srcSiteRoot.png
:width: 700px
:name: srcSiteRoot
:align: center
```

<br/>

EX : pour créer cette page j'ai dû rajouter dans le fichier "_toc.yml" une ligne du nom de "- InformationComplementaire" donc dans le dossier "src" j'ai dû créer un fichier du même nom.

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

Pour appliquer votre modification, il faut exécuter dans le terminal une suite de commandes. Pour ce faire, allez dans la barre en haut quand vous êtes sur le fichier que vous voulez modifier puis cliquez sur le terminal :

 <br/>

```{image} images/AccesTerminal.png
:width: 600px
:name: AccesTerminal
:align: center
```
<br/>

Ensuite en bas de votre application il devrait y avoir le terminal de VS code prêt à recevoir des commandes.

<br/>

```{image} images/TerminalInToFenetre.png
:width: 800px
:name: TerminalInToFenetre
:align: center
```
<br/>

Voici la première commande à entrer:

```shell
conda activate jupyter-book
```

```{note}
Cette commande sert à ce que l'on soit dans le bon environnement Anaconda. Sans ça, la commande d'après ne fonctionnera pas et on ne peut pas appliquer nos modifications.
```
ex. (ici je suis déjà sur jupyter-book): 

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

 Cela vous indique où vous vous trouvez. ensuite pour vous placer au bon endroit (si vous n'êtes pas au bon endroit) il vous suffit de taper "cd" et de glisser le dossier "src" qui contient les pages modifiées du site.
<br/>

Maintenant que vous êtes dans le bon dossier et que vous êtes sur le bon environnement (jupyter-book) vous pouvez taper la commande suivante : 
```shell
jupyter-book build .
```
<br/>
Voilà ! Une fois que tout ça est fait, vous pouvez voir le changement en local mais pas en ligne. Des modifications que vous avez apportées au fichier.

```{note}
Il suffit de copier le lien qui vous est fourni après avoir entré la commande "jupyter-book build ."
```
<br/>

```{image} images/lienSiteLocal.png
:width: 600px
:name: lienSiteLocal
:align: center
```
<br/>

Si vous voulez pouvoir voir vos modifications en ligne il faut aller sur GitHub desktop pour push (envoyer) toutes les données que vous avez modifiées. Mais avant ça il faut sélectionner le bon dossier.

<br/>

```{image} images/selectionDuBonDossier.png
:width: 400px
:name: selectionDuBonDossier
:align: center
```

<br/>

Une fois que vous êtes sur le bon dossier il faut faire un commmit à la branche principale.

<br/>

```{image} images/Commit.png
:width: 300px
:name: Commit
:align: center
```

<br/>

Une fois que c'est fait il faut cliquer sur push en haut à droite. 

<br/>

```{image} images/push.png
:width: 800px
:name: push
:align: center
```

<br/>

Ensuite vous sélectionnez le deuxième dossier et vous faites la même chose. Une fois que c'est fait vous devez aller dans le Finder et vous aller sur le dossier "src > build > html" et vous copier l'intégralité du dossier.

<br/>

```{image} images/rootToCopyHtml.png
:width: 800px
:name: rootToCopyHtml
:align: center
```

<br/>

Ensuite vous allez sur le dossier (gycha-helpdesk.github.io) et vous collez le tout dans le dossier 9adef59......

<br/>

```{image} images/rootToColler.png
:width: 700px
:name: rootToColler
:align: center
```

<br/>

Les changements prennent ~5 mins à s'appliquer, mais si vous n'êtes vraiment pas sur n'hésitez pas à refaire la commande jupyter-book build . sur VS code et à glisser les fichiers html de nouveau

<br/>

## commande qui pourrait vous être utile

Pour exécuter une commande jamf, il suffit de connecter n'importe quel ordinateur sur le réseau de l'école par câble et se rendre dans le terminal. Cette commande sert à activer toutes les règles que n'importe quel ordinateur peut recevoir.

<br/>

```{Attention}
Pour que la commande fonctionne correctement, il faut l'exécuter plusieurs fois parce qu'il y a beaucoup de règles qui sont exécutées en même temps et certaines règles dépendent d'autres règles. Du coup il est possible que l'exécuter une seule fois ne suffise pas.
```
<br/>

```shell
sudo jamf policy
```
<br/>

Si vous voulez appeler une règle précisément :

```shell
sudo jamf policy -event NomDeLaRegle
```
<br/>

```{Attention}
il ne faut pas taper exactement le nom de la regle. Il faut taper l'événement personnalisé de la règle (l'encadré en vert, en général c'est le nom de la règle). Pour vérifier si le nom de la règle et si celui de son événement personnalisé sont les mêmes il suffit de cliquer sur la règle et vérifier.


```

<br/>

```{image} images/eventPersonalise.png
:width: 1000px
:name: eventPersonalise
:align: center
```

<br/>

Cette commande sert a mettre à jour l'inventaire de jamf **de votre machine** :

```shell
sudo jamf recon 
```
<br/>

```{image} images/InvJamf.png
:width: 1000px
:name: InvJamf
:align: center
```

```shell
defaults write com.apple.dock autohide-time-modifier -float 0.5; killall Dock
```

Cette commande est plus pratique que nécessaire. En gros elle permet d'afficher plus vite la barre de menu en bas de votre mac (Le doc).

```shell
defaults write -g ApplePressAndHoldEnabled -bool false
```
Si vous avez l'habitude de maintenir la touche e pour faire apparaitre les diférentes possibilité d'accents cette commande n'est pas pour vous mais si vous voulez taper des lettres a la suite vite cette commande vous plaira ex : dddddddddddd.


Du même type si vous aller dans le réglages est que vous les régler comme l'image si dessous vous pourrez effacer a la même vitesse (comme pour vous déplacer).

```{image} images/KeyParam.png
:width: 700px
:name: KeyParam
:align: center
```

<br/>

## Ordinateur de prêt

Pour configurer un ordinateur a prêter il faut commencer en lui [installant](https://support.apple.com/fr-ch/HT211683) l'OS qu'il supporte (Catalina pour 2012 et Big Sur pour 2014). Sur ce site il y a toutes les informations et version. De macOS High Sierra jusqu'à macOS Ventura. Ensuite il faut vérifier que l'ordinateur n'a pas plusieurs disques. Si c'est le cas il faut aller dans "utilitaire de disques" et supprimer ceux en trop et en garder un seul (chamblandesHD). 
<br/>

```{image} images/DiskUtility.png
:width: 400px
:name: DiskUtility
:align: center
```

<br/>

Ensuite, il faut appliquer les règles de jamf (sudo jamf policy). Il faut vérifier que dans les applications l'ordinateur a bien Outlook, Teams, Word, etc. Une fois que vous avez fait toutes ces étapes il ne reste plus qu'a créer un compte admin (user : adminl et Mdp : Gym _09). Il ne faut pas oublier son compte (un compte utilisateur) et modifier dans le teams le fichier inventaire en classifiant l'ordinateur par rapport a son nom.

## Schéma réseau des salles de classe en général

VLAN :

- 34 = serveur.
- 48 - 49 = ordinateur personel.
- 40 = Poste de l'école. (wifi)
- 38 = Imprimante
- 32 = materiel infra (switch, etc)

<br/>

Voici les switchs réseau que vous retrouverez dans toutes les salles de classe. 

<br/>

```{note}
Le port 1 est pour internet, le port 2 pour le mac mini (le Pc fixe), le port 3 le beamer, le port 8 c'est pour les ordinateurs personnels des profs.
```

<br/>

```{image} images/avantSwitchReseau.jpg
:width: 600px
:name: avantSwitchReseau
:align: center
```
<br/>

Comme on peut le voir à l'arrière il n'y a que l'alimentation.

```{image} images/ArierreSwitchReseau.jpg
:width: 600px
:name: ArierreSwitchReseau
:align: center
```
<br/>

```{note}
Normalement a l'avant il y a juste le bouton power et input, le bouton input change quel câble hdmi sera affiché au beamer. Comme on peut le voir sur l'in 1 ça sera la Wacom donc l'ordinateur fixe (le mac mini). In 2 ordis perso donc l'ordinateur que le prof amène ou les élèves. In 3 c'est pour la caméra qui est dans la salle.
```

<br/>

```{image} images/AvantSwitchHDMI.jpg
:width: 600px
:name: AvantSwitchHDMI
:align: center
```
<br/>

```{note}
Le port HDMI "output" c'est le câble HDMI qui relie le beamer (il sert de sortie pour toutes les autres entrées hdmi), l'in 3 est relié à la caméra, l'in 2 à l'ordi perso, et l'in 1 au mac mini.
```

<br/>

```{image} images/arriereSwitchHDMI.jpg
:width: 600px
:name: arriereSwitchHDMI
:align: center
```

<br/>

```{note}
Sur le mac mini ce n'est pas compliqué même s'il en donne l'impression. Tout à gauche c'est l'alim du mac mini, ensuite c'est le câble réseau donc internet (sur la photo c'est le câble rouge). Après tout le reste est relié ensemble jusqu'au même câble. Sur ce même câble il y a le câble HDMI du mac mini, un câble USB (il sert à relier les ports USB de la Wacom au mac mini s'il y en a) et pour finir l'alim de la Wacom et tous ces câbles sont réuni en un seul et il est connecté à la wacom.
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

## Fonction / schéma de l'usi / dgep / dgnsi

Pour gérer le support des écoles post obligatoires ils ont créé un système en suivant le modèle d'ITIL.

Donc pour commencer toutes les écoles ont un helpdesk (le niveau 1) si les commandes dépassent notre compréhension ou si elles dépassent notre domaine d'action. Le niveau 2 c'est l'USI, le niveau 3 c'est les ingénieurs qui sont aussi a l'USI mais c'est une autre partie et pour finir il y a le niveau 4 qui est le fournisseur des applications ou des services.

<br/>

```{note}
Sur le schéma on peut constater qu'une personne exécute plusieurs fonctions en même temps, Simplement c'est le chef de l'USI donc il a plusieurs postes.
```

<br/>

```{image} images/USI.png
:width: 800px
:name: USI
:align: center
```

<br/>

```{note}
L'USI peut aussi accéder au serveur SQL et y exécuter des commandes.
```

<br/>

```{image} images/ShemaDGEP.png
:width: 600px
:name: ShemaDGEP
:align: center
```

<br/>


## Informations supplémentaire

### kahoot

Sur kahoot il est possible de lancer en boucle un quiz. Pour ce faire il faut accéder à la bibliothèque ou sont organisés tous vos quiz. Ensuite cliquez sur jouer (sélectionnez le quiz que vous voulez lancer en boucle).

<br/>

```{image} images/kahootBiblioJouer.png
:width: 1000px
:name: kahootBiblioJouer
:align: center
```

<br/>

 Ensuite une pop-up s'affichera avec deux modes de jeu, choisissez celui de gauche.

<br/>

```{image} images/KahootModeDeJeu.png
:width: 600px
:name: KahootModeDeJeu
:align: center
```

<br/>

Une fois le mode de jeu choisi il faut aller dans les options pour les afficher en selectionnant [passer automatiquement les questions](https://support.kahoot.com/hc/fr/articles/115016055107-Options-de-jeu-en-direct#auto_move) des questions. 

<br/>

```{image} images/KahootOptionDeJeu.png
:width: 600px
:name: KahootOptionDeJeu
:align: center
```
### VMware / vSphere

[Comment se connecter a vSphere](https://vcenter.dgep.edu-vaud.ch/ui/#?extensionId=vsphere.core.inventory.serverObjectViewsExtension&objectId=urn:vmomi:VirtualMachine:vm-127617:93734f74-49db-4644-be85-8dab90d13b02&navigator=vsphere.core.viTree.hostsAndClustersView)

<br/>

```{image} images/VsphereConnection.png
:width: 400px
:name: VsphereConnection
:align: center
```

<br/>

Sur vSphere il y a une notation un peu spéciale que vous pourrez retrouver ici :

- DUS = DC (Domain Controller)
- NGE = Network (DHCP, NPS, FFSO)
- PGE = Printer (papercut)

<br/>

```{image} images/VsphereInterface.png
:width: 400px
:name: VsphereInterface
:align: center
```

<br/>

### Site de vente / achat et imprimante


L'ancien nom du site de "vente, achat" de matériel pour les établissements post obligatoire s'appelait "le Dol". Maintenant ils ont changé pour "la place".

```{note}
Les écoles post obligatoire ont des rabais immenses sur les licences, le matériel etc. (chez Dell ça peut aller jusqu'à du 60% voir plus). Ils ont des licences office pouvant aller jusqu'à 5.- par personne.
```
<br/>

Pour dépanner les imprimantes en général c'est parce que la personne a mal tapé son mot de passe du coup il faut réafficher le pop-up et pour ça il faut soit relancer une impression soit cliquer en bas à gauche de l'écran ensuite il faut cliquer sur la petite flèche et normalement ça réaffichera le pop-up.

<br/>

Si rien de tout ça ne marche alors vous pouvez aussi redémarrer le serveur d'impression.

<br/>

```{image} images/SrvPrint.png
:width: 800px
:name: SrvPrint
:align: center
```

<br/>

si le redémarrer ne marche pas non plus vous pouvez aller dans "tools" puis "print management". Ensuite cliquer sur "All Printer". Dans cette interface vous pouvez régler plusieurs choses notamment supprimer les impressions en file d'attente, etc...

<br/>

```{image} images/InSrvPrint.png
:width: 800px
:name: InSrvPrint
:align: center
```

<br/>

#### Ajouter l'imprimante du bureau.

aller dans imprimantes et scanners.

ensuite cliquer sur le petit **+** . Ensuite clique droit sur la barre puis sélectionner personnaliser. ensuite il faut glisser déposer les options avancées dans la barre de recherche 

<br/>

```{image} images/ImpBureau.gif
:width: 700px
:name: ImpBureau
:align: center
```

<br/>

Parfais ensuite il faut configurer comme suit : 

```{image} images/ReglageImp.png
:width: 600px
:name: ReglageImp
:align: center
```

<br/>

et voilà il faut juste cliquer sur ajouter et vous avez rajouté l'imprimante du bureau.

### Problème d'affichage quand on créé une section sur le site


Quand on créé une section pour la première fois si vous ne voulez pas qu'il y ai un problème d'affichage. 

<br/>

```{image} images/JeSuisUnBug.gif
:width: 800px
:name: JeSuisUnBug
:align: center
```

<br/>

```{note}
Pour pouvoir mettre un gif sur le site j'ai utilisé un site de [conversion](https://cloudconvert.com/) de fichier .mov en .gif (les fichiers .mov c'est les fichiers quand tu fais une vidéo de ton écran). Ensuite tu les places dans le dossier images du site et voilà
```

<br/>

il faut impérativement exécuter la commande suivante si vous voulez régler le problème : 

```shell
jupyter-book clean .
```

```{Attention}
pour que la commande fonctionne il faut que vous soyez dans le bon dossier (celui du site). Au même endroit que pour rexecuter la commande jupyter-book build .
```

```{Attention}
Ensuite il faut absolument exécuter la commande : 
```

```shell
jupyter-book build .
```

### Groupe d'élève / Son dans les salles 

En générale un élève dervais avoir tout ces groupes :

<br/>

```{image} images/GroupeEleve.png
:width: 400px
:name: GroupeEleve
:align: center
```

<br/>

Si vous voyez qu'il n'a pas tous les groupes, appelez votre maître de stage et demandez-lui si vous pouvez rajouter les groupes manquant manuellement.

<br/>

Dans les salles de classe il y a 2 manières de comment le son fonctionne. 

1. La première c'est qu'il  y a dans les salles de classe une / un empli qui permet d'émettre du son et dans ce cas il n'y a pas besoin d'allumer le beamer mais il faut se connecter dessus avec soi ordinateur perso soit avec le mac mini mais a disposition dans les salles. (si ça ne marche pas il faut vérifier la source sur l'emplir). en général c'est tablette ou un truc du genre. Si ça ne marche pas aller dans les préférence et vérifier que la sortie soit la bonne


Voilà a quoi resemble une / un empli dans une salle de classe.

```{image} images/SonSalleDeClasse.jpg
:width: 600px
:name: SonSalleDeClasse
:align: center
```

<br/>

2. La deuxième option c'est qu'il n'y a pas d'empli et dans ce cas la il faut allumer le beamer qui va lui se connecter automatiquement au haut-parleur qui est dans les salles de classe et émettre du son. (Si ça ne marche pas il faut aller dans préface système, est sélectionné la 3ème source : la 1 c'est le mac mini en général c'est marquer interne quelque chose, la 2 c'est la Wacom en général c'est DTK-des chiffres, du coup il faut sélectionner la 3ème).

### Recherche JAMF 


Si vous lancez jamf pour **la première fois** il est possible que vous **ne puissiez pas effectuer des recherches** quand vous êtes sur "ordinateur". Pour résoudre le problème c'est très simple.

Aller sur Jamf, ensuite cliquer sur votre profil

<br/>

```{image} images/RecheJamf.png
:width: 800px
:name: RecheJamf
:align: center
```

<br/>

Ensuite il faut aller sur préférence de recherche est modifié si vous êtes en "Exact match" en "contains"

<br/>

```{image} images/PrefRecheJamf.png
:width: 500px
:name: PrefRecheJamf
:align: center
```
<br/>


### DashBoard jamf


Quand vous vous connectez à Jam vous arriver par défaut sur le dash board. Sur cette fenêtre il sera affiché toutes les règles que vous avez en "favoris" cela permet de suivre leur avancement, est d'observer graphiquement plusieurs informations. 

<br/>

```{note}
Vous pouvez mettre plusieurs règles, et pour voir plus d'informations il suffit de cliquer sur la règle.
```

<br/>

```{image} images/DashBoard.png
:width: 700px
:name: DashBoard
:align: center
```

<br/>

Pour mettre une règle en "favoris", il faut que vous recherchiez votre règle. Une fois que vous êtes dessus **en haut à droite** il y a une case à cocher, il suffit de la cocher est quand vous retournerez au dashboard votre règle serra afficher.


```{image} images/CheckBoxFavorisJamf.png
:width: 1100px
:name: CheckBoxFavorisJamf
:align: center
```

### Comment modifier le fichier inventaire.


Pour commencer il faut aller sur teams.  Dans l'équipe GychaIT > ensuite dans le groupe > gestion de postes > File > le dossier de l'année corespondantes.

```{image} images/RootTeamsInv.png
:width: 900px
:name: RootTeamsInv
:align: center
```

<br/>

Ensuite faites les modifications que vous voulez. Une fois fini il faut mettre ce fichier sur le serveur en remplaçant l'autre fichier déjà existant : 

```{image} images/RootSRVinv.png
:width: 900px
:name: RootSRVinv
:align: center
```

<br/>

Ensuite il faut lancer le script python qui va renter les données dans un autre fichier.

<br/>

Normalement dans votre terminal vous devriez avoir quelque chose de similaire.

```{image} images/ScriptInv.png
:width: 800px
:name: ScriptInv
:align: center
```

<br/>

```{note}
Le script pyton est au même endroit que le fichier excel inventaire. Pour le lancer il faut aller dans le terminal, aller au même endroit ou le script est en utilisant : (cd leCheminOuSeTrouveLeScript)
```

une fois que vous êtes dans le bon dossier il faut exécuter cette commande :

```shell
python3 LeNomDuScript
```

<br/>

Pour vérifier que vos changements on bien est effectué il faut aller sur le seveur et regarder le fichier


```{image} images/RootVerification.png
:width: 900px
:name: RootVerification
:align: center
```


## Mettre en ligne des vidéo sur YouTube / Imovie


Avant de commencer il vous faut Imovie et une chaîne Youtube.

<br/>

Sur Imovie pour créer un projet il faut cliquer sur le + et ensuite cliquer sur le film. **(si quand vous ouvrez Imovie pour la première fois et que vous n'êtes pas sur la bonne fenêtre il faut cliquer sur projet en haut à gauche de l'écrant)**.


```{image} images/CreationFilmImovie.png
:width: 300px
:name: CreationFilmImovie
:align: center
```

<br/>

```{Attention}
Même si vous avez créé un nouveau projet vous pourrez quand même modifier les autres.
```

```{note}
Il y a aussi une banque d'images et de son
```

1. Ici vous retrouverez tous les projets vidéo que vous avez.


2. C'est le curseur qui permet que quand vous lancer la vidéo elle se lance la ou le curseur et placé.


3. Ici vous verrez tous les fichiers son ou image ou je ne sais quoi que vous aurez soit drag and drop soit importé. Vous pouvez faire beaucoup de choses avec un clique droite, comment par exemple ajuster le volume du son ou encore couper la vidéo ou mettre des transitions. bref il y a beaucoup de possibilités. Vous pouvez même accélérer la vidéo.


4. Fichier son


5. Cette règle permet de modifier **la taille d'affichage** des fichiers audio et vidéo.


6. Quand vous double cliquer sur une image vous pouvez choisir un point de départ et un point d'arrivée pour pouvoir créer des effets pendant la vidéo. (Des effets de zoom ou d'effet de droite à gauche)

```{image} images/InterfaceImovie.png
:width: 900px
:name: InterfaceImovie
:align: center
```

<br/>

Une fois que vous avez fini votre projet il faut que vous cliquiez sur **"projets"** en haut a gauche. Pour que vous lui donniez un nom.

Ensuite pour télécharger votre vidéo il faut cliquer sur les 3 petits point **"..."** ensuite sur **"partager le projet"**, et pour finir sur **"fichier"**


```{image} images/ImportImovieFilm.png
:width: 600px
:name: ImportImovieFilm
:align: center
```

<br/>

Ensuite une fenêtre apparaîtra avec plusieurs options je vous conseille de mettre la résolution à 720p (ça suffit largement). Le reste à vous de jugé si vous le voulez ou pas.

```{image} images/ReglImovieFilm.png
:width: 600px
:name: ReglImovieFilm
:align: center
```

<br/>

Voilà vous savez plus ou moins utiliser Imovie. Maintenant on va passer à la mise en ligne de la vidéo sur Youtube.

Tout d'abrod il faut que vous vous rendiez sur Youtube Studio (ça permet de gérer vos chaînes YT). Quand vous êtes dessus il faut que vous appuyer sur le menu à gauche **"Tableau de bord"**. Puis **"importer des vidéos**.


```{image} images/YTStudio.png
:width: 800px
:name: YTStudio
:align: center
```

<br/>

Ensuite vous sélectionner votre fichier qu'Imovie vous a fourni puis vous le drag and droper ou alors vous aller le chercher au bon emplacement.
Une fois que vous avez sélectionné le bon fichier vous arriverez sur cette fenêtre :

sur cette fenêtre vous aurez 2 choses a changer la première c'est que la vidéo n'est pas conçue pour des enfants (sauf si c'est le cas). Ensuite vous cliquez sur **"Plus"**

<br/>

```{image} images/YTLimiteAge.png
:width: 700px
:name: YTLimiteAge
:align: center
```

<br/>

Ensuite vous descendez tout en bas de la page et vous sélectionner Desactivier les commentaires. (je fais ça uniquement pour éviter les mauvaises surprises du genre troll ou insulte envers la personne qui parle).


```{image} images/YTComm.png
:width: 700px
:name: YTComm
:align: center
```

<br/>

Après ça vous attendez que votre vidéo finisse de charger et que Youtube finisse de vérifier que votre vidéo est conforme à leurs règles. (cette opération peut prendre quelques minutes). Ensuite vous cliquez sur le suivant, suivant, suivant jusqu'à arriver au dernier point. Et vous cochez la case **"non répertoriée"**.


```{note}
Cela permet de ne pas retrouver la vidéo quand vous effectuez une recherche sur Youtube.
```

<br/>

```{image} images/YTNonrepe.png
:width: 700px
:name: YTNonrepe
:align: center
```

<br/>

Cliquer sur terminer et revenez sur la page de Youtube Studio, dans le menu a gauche sélectionner **"Contenu de la chaîne"** et vous pourrez effectivement voir que votre vidéo a été mise en ligne et quelle est en mode **"non répertoriée"**.


```{image} images/YTVerification.png
:width: 700px
:name: YTVerification
:align: center
```

<br/>

## Créer un PDF du site à partir de jupyter-book

Il est possible de créer un PDF à partir du code HTML de votre book. 

### Installation



Votre système devra utiliser pyppeteerpour analyser le HTML généré pour la conversion en PDF.

Vous pouvez l'installer comme ceci :


```shell
pip install pyppeteer
```


Vous devrez peut-être également installer cet ensemble de packages ci-dessous (sur les systèmes * nix (dans le doute je l'ai installé)):

```shell
gconf-service
libasound2
libatk1.0-0
libatk-bridge2.0-0
libc6
libcairo2
libcups2
libdbus-1-3
libexpat1
libfontconfig1
libgcc1
libgconf-2-4
libgdk-pixbuf2.0-0
libglib2.0-0
libgtk-3-0
libnspr4
libpango-1.0-0
libpangocairo-1.0-0
libstdc++6
libx11-6
libx11-xcb1
libxcb1
libxcomposite1
libxcursor1
libxdamage1
libxext6
libxfixes3
libxi6
libxrandr2
libxrender1
libxss1
libxtst6
ca-certificates
fonts-liberation
libappindicator1
libnss3
lsb-release
xdg-utils
wget
```
### Appliquer les commandes / construire le PDF

Pour créer un seul PDF à partir du code HTML de votre book, utilisez la commande suivante :


```shell
jupyter-book build . --builder pdfhtml
```
ou

```shell
jb build . --builder pdfhtml
```

Voilà ensuite rendez-vous dans vore dossier Src > build > PDF et vous y retrouverez le PDF


```{image} images/rootToPDF.png
:width: 800px
:name: rootToPDF
:align: center
```

## Rajouter des imprimantes avec CUPs 2.3.4

```{note}
> - Tout d'abord il faut aller sur un navigateur est tapez l'adresse suivante : localhost:631
> - voici la commande pour afficher l'interface graphique de cups et potentiellement régler des problèmes de connexion au site : cupsctl WebInterface=yes 
> - Attention pour pouvoir rajouter des imprimantes où simplement utiliser cups il faut que pour pouvoir se connecter sur votre machine avec un compte qui a un mot de passe. Sinon vous serez bloqué, car cips demande le mdp du user de la session.
```
<br/>

Normalement vous devrez arriver sur cette page (voir ci-dessous). Si c'est le cas cliquer sur **"administration"**

<br/>

```{image} images/homepage.png
:width: 700px
:name: homepage
:align: center
```
<br/>

Une fois que vous avez cliqué sur **"administration"**. La page ci-dessous devrait s'afficher. Une fois que vous êtes sur cette page il vous faut cliquer sur Add printer.

```{image} images/administrationPage.png
:width: 700px
:name: administrationPage
:align: center
```

```{note}
Si vous cliquez sur manage Printer vous pouvez modifier les paramètres que nous allons modifier lors de la création et vous pourrez voir toutes les imprimantes que vous avez rajoutées.
```

<br/>

```{image} images/AddPrinter.png
:width: 700px
:name: AddPrinter
:align: center
```

Selectionné **"LPD/LR Host or Printer"** ensuite cliquer sur **"continue"**.

<br/>

Ensuite vous arriverez sur cette fenêtre. Ici il faut noter la même chose qu'avant donc : **lpd://gycha-srv-prt01/gycham- La salle de l'imprimante - le driver utiliser**. Puis cliquer sur continue.

```{image} images/AdressPrinter.png
:width: 700px
:name: AdressPrinter
:align: center
```

<br/>

Sur l'image ci-dessous, recopier le nom en mettant le bon nom 

<br/>

```{attention}
Sur l'image, à droite de (Connexion: juste après l'a18 il y a 2 tirets "- -", c'est une erreur de ma part).
```

<br/>

```{image} images/PrinterName.png
:width: 700px
:name: PrinterName
:align: center
```

<br/>

Maintenant il faut sélectionner **"HP"** et cliquer sur continue (sur l'image ci-dessous)


```{attention}
Il ne faut pas cliquer sur "choisir un fichier ni Add Printer" 
```

```{image} images/DriverPrinter.png
:width: 700px
:name: DriverPrinter
:align: center
```

<br/>

ensuite sélectionner le bon driver (celuil qui correspond à votre imprimante donc : pour les HP3015 c'est le p3010 pour le PHM506 c'est le M506, pour le HPM552 c'est le M552 etc...)


```{image} images/DriverSelection.png
:width: 700px
:name: DriverSelection
:align: center
```

<br/>

Sur la prochaine fenêtre il faudra changer plusieurs petits paramètres pour permettre l'impression recto-verso et valider le format de l'impression.


```{image} images/OptionInstalled.png
:width: 700px
:name: OptionInstalled
:align: center
```
sur l'image ci-dessus il faut cocher "installé" pour "l'accessoire d'impression recto-verso". ensuite cliquer sur Général (le bouton est en bleu).


<br/>

```{image} images/OptionGeneral.png
:width: 700px
:name: OptionGeneral
:align: center
```

sur l'image ci-dessus il faut sélectionner **"Reliure sur bord long"** pour "recto-verso" et si ce n'est pas déjà fait il faut sélectionner **"à4"** dans "format de page".

<br/>

Pour accéder à la page suivante il faut cliquer sur "Finishing panel". Ensuite il faut modifier "le papier pour brochure" et le mettre en **"a4"**

```{image} images/OptionFinition.png
:width: 700px
:name: OptionFinition
:align: center
```

```{attention}
Il ne faut surtout pas oublier de cliquer sur SET DEFAULT OPTION pour que les modifications soient sauvegardées.
```

```{attention}
Les imprimantes des salles de dessin et de la salle des maîtres utilise des drivers différents car ce sont des imprimantes cannon et non pas HP comme le reste du gymnase. (Sdm-est = c5535/5540), (sdm-ouest et sdm-nord = 6555/6565). Le paramétrage et aussi un peu différent.
```

<br/>

```{image} images/sdm-est.png
:width: 700px
:name: sdm-est
:align: center
```

<br/>

```{attention}
- Image du dessus = SDM-EST
- Image du dessous = SDM-NORD
```

<br/>

```{image} images/sdm-Nord.png
:width: 700px
:name: sdm-Nord
:align: center
```

<br/>

## Ajouter une imprimante sur le serveur et lui attribuer une adresse IPV4 fixe.

<br/>

Pour ajouter une imprimante sur le serveur et lui attribuer une adresse IPV4 fixe est plutôt simple. Avant de commencer vérifier que vous avez accès au serveur DHCP et que vous avez également accès au serveur d'impression. Une fois que c'est bon vous pourrez commencer. Tout d'abord il faut aller sur le serveur d'impression (celuil du milieu). Voir image ci-dessous. (PrintServe).

<br/>

```{image} images/SRVprinter.png
:width: 900px
:name: SRVprinter
:align: center
```

<br/>

Une fois que vous êtes connecté au serveur d'impression aller dans la console de management et aller dans l'onglet print management. Normalement vous devriez avoir quelque chose de similaire à la capture d'écran ci-dessous. Maintenant que vous êtes ici, cliquer sur (Print Serveurs) et ensuite cliquez droit sur "Printer" puis "add Printer..."

<br/>

```{image} images/Srv_add_printer.png
:width: 400px
:name: Srv_add_printer
:align: center
```

<br/>

Pour la suite il faut "juste" cliquer sur next - next - next, c'est assez logique (si vous avez des doutes demander à David par précaution). À un moment donné par exemple il faut savoir ladresse IP de l'imprimante que vous voulez rajouter, en bref ce n'est pas super-compliquée mais si vous avez de doute vous pouvez toujours demander à David. Maintenant que vous l'avez rajouté sur le serveur d'impression il faut lui attribuer une adresse IPV4 fixe est pour ce faire il faut aller dans le DHCP.


```{attention}
Si vous essayer d'aller sur le DHCP qu'il y a sur le serveur AD ça ne va pas marcher, je sais pas pourquoi. (Il faut demander à David pourquoi ça ne marche pas).
```

Du coup il faut ajouter un "serveur DHCP" sur remonte desktop. Pour le faire il y a une marche à suivre quelques pars sur ce site mais je vais vous réexpliquer comment faire. Il fut vous rendre sur la remonte desktop, et cliquer sur add PC.

<br/>

```{image} images/AddSRVDHCP.png
:width: 600px
:name: AddSRVDHCO
:align: center
```

<br/>

Une fois que vous avez cliqué sur "add PC" Il faut juste mettre l'adresse IP du serveur en question et de lui donner un nom cohérent dans mon cas DHCP me convient parfaitement. normalement le reste des paramètres ne doit pas être changé, en gros vous laisser les paramètres par défaut mais vérifier quand même par rapport à ce que j'ai mis. 

<br/>

```{image} images/ConfigDHCPServeurToadd.png
:width: 400px
:name: ConfigDHCPServeurToadd
:align: center
```

<br/>

Maintenant vous devriez le voir apparaître dans la fenêtre sur remote desktop. Cliquer dessus (il nous reste quelque petit Réglages à faire).

<br/>

```{image} images/dhcp1.png
:width: 900px
:name: dhcp1
:align: center
```

<br/>

Une fois que vous êtes connecté sur votre serveur dchp, rechercher le/la **"console management"** dans la barre de recherche si elle n'est pas déjà ouverte, puis aller sur **tools > DHCP**. Ensuite dans l'onglet DHCP sélectionner **"IPv4"** et ouvrez le dossier **"Scope Imprimantes"** puis cliquer droit sur **"réservation"**. Ensuite cliquer sur **"New Reservation..."**.

<br/>

```{image} images/dhcp2.png
:width: 500px
:name: dhcp2
:align: center
```

```{image} images/dhcp3.png
:width: 400px
:name: dhcp3
:align: center
```

<br/>

```{note}
Si vous voulez mettre une nouvelle imprimante mais garder le nom de l'ancienne (par exemple quand on remplace une imprimante dans une salle de classe). Vous pouvez, il faut juste que dans le paramètre de l'image ci-dessous vous mettez e même nom.
```


<br/>

```{image} images/dhcp4.png
:width: 400px
:name: dhcp4
:align: center
```

<br/>


