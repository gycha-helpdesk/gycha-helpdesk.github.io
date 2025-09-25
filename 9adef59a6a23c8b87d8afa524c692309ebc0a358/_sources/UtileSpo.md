<!--
Auteur : [À compléter]
Date : [À compléter]
Description : Documentation d’utilisation du script Semaine Silence On Lit
-->

# Documentation — Semaine Silence On Lit

> **Objectif** : Automatiser la lecture de fichiers audio (.mp3) à des horaires précis pour l’événement « Silence On Lit ».

---

## Organisation des dossiers

Sur le bureau, il y a deux dossiers :

- `scripte_musique`
- `musique`

```{image} images/spo1.png
:width: 800px
:name: spo
:align: center
```

---

## Lancer le script

1. Ouvrez un terminal.
2. Déplacez-vous dans le dossier du script :

    ```bash
    cd ~/Desktop/scripte_musique
    ```

3. Lancez le script :

    ```bash
    python3 music.py
    ```
```{image} images/spo2.png
:width: 800px
:name: spo
:align: center
```

---

## Fonctionnement

- Les fichiers audio (.mp3) doivent être placés dans le dossier `Musique`.
- Ils seront lus par ordre alphabétique.

```{image} images/spo3.png
:width: 600px
:name: spo
:align: center
```

---

## Configuration des horaires de lecture

Pour modifier les horaires de lecture des fichiers :

- Rendez-vous aux lignes 74 à 78 du script.
- La première ligne indique que le premier fichier mp3 sera lu à 07h40, la deuxième ligne que le deuxième fichier sera lu à 10h15:20, etc.  
Vous pouvez ainsi définir l’heure de lecture de chaque fichier mp3.
- Exemple :

    ```python
    (allMp3Files[0], "07:40:00"),
    (allMp3Files[1], "10:15:20"),
    (allMp3Files[2], "10:30:00"),
    # Ajouter ici d’autres fichiers si besoin
    (allMp3Files[3], "10:35:00"),
    ```

- Ajoutez une ligne par fichier supplémentaire.

```{image} images/spo4.png
:width: 800px
:name: spo
:align: center
```
---

## Configuration des dates de début et de fin

- Rendez-vous aux lignes 82 à 84 du script.
- Modifiez les dates de début et de fin selon vos besoins (possible sur plusieurs jours).

```{image} images/spo5.png
:width: 800px
:name: spo
:align: center
```
---


---

