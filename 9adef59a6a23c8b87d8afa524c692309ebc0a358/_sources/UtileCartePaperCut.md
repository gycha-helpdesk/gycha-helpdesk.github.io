# Les Cartes Papercut

## Exécution du script et importation des cartes

Il faut juste télécharger le dossier puis exécuter le script python. Quand vous lancerez
le script, il va vous demander le nombre de carte que vous voulez faire et la valeur de
chaque carte en CHF, puis le script va sortir un csv qui ne faut surtout pas toucher ni
ouvrir et un PDF avec les cartes à imprimer.

```{image} images/cartepapercut1.png
:width: 500px
:name: jamfRuleDashboard
:align: center
```


Dans Papercut, il faut se connecter avec son compte administrateur, puis aller sur
l’onglet “Cartes”. Sur la droite il y a “Action” et il faut sélectionner “Importer de
nouvelles cartes”.


```{image} images/cartepapercut2.png
:width: 500px
:name: jamfRuleDashboard
:align: center
```

### 1

Sur la page “Importer Numéros de carte”, il faut juste choisir le csv du script qui
s’appelle “importFile.csv” et télécharger.

```{image} images/cartepapercut3.png
:width: 500px
:name: jamfRuleDashboard
:align: center
```

Et finalement sur la page “Cartes” il y aura les nouvelles cartes qui seront prêtes à être
utiliser.



## Utiliser les cartes

Pour utiliser les cartes il faut aller sur Papercut en tant qu’utilisateur et sur la page
“Utiliser une carte prépayée” et entrer le numéro de la carte qui est la date de
création et un numéro aléatoire.

```{image} images/cartepapercut4.png
:width: 500px
:name: jamfRuleDashboard
:align: center
```

### 2

# Détail du script

La partie à adapter selon vos besoins se trouve aux lignes 70- 96 qui construise le PDF
à imprimer qui a les cartes à distribuer.
À la ligne 73, il y a notre logo qui est dans le dossier qui faut juste remplacer.
À la ligne 74, il y a le titre qui sera sur les cartes (pour nous c’est “Recharge
impression Konica Minolta salle A301“).
De la ligne 83 à 89, nous avons les explications pour utiliser les cartes qui faudra
adapter pour votre infrastructure.
De la ligne 90 à 91, il y a un rappel sur les frais d’impression.

# Bon à savoir

Si dans le script vous voulez modifiez le code que les utilisateurs doivent rentrer, il y a
un format spécifique qu’il doit y avoir que nous ne connaissons pas très bien sinon la
DB des cartes plante. Donc il faut éviter de toucher à cette partie.

Actuellement avec le script il peut faire un lot par jour, car le code contient la date du
jour de création et pas avec les minutes et les secondes.

Les cartes expirent le prochain 31 juil. si vous voulez modifier ce fonctionnement il se
trouve à aux lignes 59- 62

Il ne faut pas ouvrir ni modifier le csv crée par le script car il devient inutilisable, donc
il faut refaire le script pour ravoir un csv qui fonctionne.


