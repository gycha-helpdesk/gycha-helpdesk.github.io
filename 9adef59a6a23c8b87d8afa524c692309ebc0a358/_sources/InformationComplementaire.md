# Information complémentaire

> Dans cette partie du site je vais vous explique comment mettre ajour le site / rajouter du contenu.
> en paralelle je vais vous donnez plein d'information concernant les panes que vous pourrez rencontrez.
> je vais aussi vous expliquer le fonctionnement de l'usi, la dgnsi, la dgep, la dgo et les outils qui sont a notre dispotition.

## Mettre a jour et modifier le site 


Tout d'abord il faut que vous puissez ouvrire les fichiers sur un logiciel de code (j'utiliser visual studio) ensuite il faut que vous vous rendiez dans le finder,
Dans le dossier "src" du site. c'est dans ce dossier que vous allez soit modifiez des fichier existant soit en rajouter. pour le modifier il suffit d'ouvir un fichier qui existe déjà et de le modifier.

```{note}
Pour faire des capture d'écrant il faut appuyer sur : commande, MAJ, 4
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

donc si vous ne savez pas ou vous êtes taper : 
```shell
    pwd
```
<br/>

dans le terminal est cela vous indique ou vous vous trouvez. ensuite pour vous placer au bon endroit (si vous n'etez pas au bon endroit) il vous suffit de taper "cd" et de glisser le dossier dans lequel vous voulez vous trouvez dans le terminal.
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

si ça ne marche pas du premier coup faite toutes ces actions une deuxième fois. ça dévrais marcher. (c'est parce que il y a des dossier qui dépendent d'autre dossier du coup il faut en générale le faire 2 fois)