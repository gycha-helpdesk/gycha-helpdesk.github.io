# Créer un groupe intelligent Jamf

Les groupes intelligents permettent de créer des groupes de postes selon des critères données.
Par exemple, si je veux grouper tous les ordinateurs de la c06 sans avoir à les ajouter un à un manuellement,
je peux créer un groupe intelligent qui contient tous les ordinateurs "C06-". 

Ca peut etre très utile pour des règles jamf, pour cibler un groupe de poste plus facilement et que le groupe se mette à jour automatiquement si on ajoute des postes dans la salle etc.

# Création du groupe intelligent

Pour ce faire, il faut aller sous Ordinateurs > Groupes > Groupes d'ordinateurs intelligents et cliquer sur Nouveau+

```{image} images/addIntelligentGroup.png
:width: 500px
:name: addIntelligentGroup
:align: center
```

Ensuite, vous allez devoir mettre un nom de groupe, puis après choisir les critères pour que des postes soit ajoutés au groupe:

En cliquant sur ajouter, vous avez la liste de critères utilisables pour ajouter des postes: Le nom de l'ordinateur, l'OS, le type de processeur...

```{image} images/intelligentCriteria.png
:width: 500px
:name: intelligentCriteria
:align: center
```

Si on choisit "Computer name" par exemple, on peut décider que le nom corresponde à certains critères: like, not like, match,... par rapport a la valeur que l'on souhaiterait mettre.

```{image} images/intelligentCriteria.png
:width: 500px
:name: intelligentGroupValue
:align: center
```

Quand le groupe intelligent est créé, on peut voir quels ordinateurs ont été ajoutés en cliquant sur "Afficher" en bas à droite.



