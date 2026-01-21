<!--
Author:         Gycha IT
Date:           2024-06-13
Description:    Guide pour affichage automatique de photos & vidéos sur Raspberry Pi
-->

# MAJ TEAMS 

## 📂 Emplacement des fichiers

| Type               | Chemin                                                  |
|--------------------|----------------------------------------------------------|
| Script Python      | `/home/gycha/.media/media_display.py`                   |
| Service systemd    | `/etc/systemd/system/media_display.service`             |
| Bloc 1 – images    | `/home/gycha/.media/bloc1/images/`                      |
| Bloc 1 – videos    | `/home/gycha/.media/bloc1/videos/`                      |
| Bloc 2 – images    | `/home/gycha/.media/bloc2/images/`                      |
| Bloc 2 – videos    | `/home/gycha/.media/bloc2/videos/`                      |
| Images (défaut)    | `/home/gycha/.media/images/`                            |
| Videos (défaut)    | `/home/gycha/.media/videos/`                            |
| Fichier texte      | `/home/gycha/.media/texte.txt`                          |

```{image} images/rasp_01.png
:width: 1000px
:name: raspberry
:align: center
```

---

## 🚀 Lancement automatique

Le script démarre automatiquement au démarrage du Raspberry Pi grâce à un service `systemd`.

- Adresse : `gycha@gycha.local`  
- Utilisateur : `gycha`  
- Mot de passe : gycha_2025*

---

## ▶ Commandes utiles

### Démarrer manuellement le script

```bash
sudo systemctl start media_display.service
```

### ⏹ Arrêter le script

```bash
sudo systemctl stop media_display.service
```

*Attention : cela peut prendre 2-3 minutes.*

### 🔄 Redémarrer le script

```bash
sudo systemctl restart media_display.service
```

---

## 📤 Copier des fichiers depuis un Mac vers le Raspberry Pi

### ✅ Étapes recommandées

1. Crée un dossier `images` et un dossier `videos` sur ton bureau Mac.
2. Exécute les commandes suivantes dans **un nouveau terminal** (ne pas être connecté en SSH).

### 🔁 Copier dans `bloc1`

#### Images

```bash
scp ~/Desktop/images/* gycha@gycha.local:/home/gycha/.media/bloc1/images/
```

#### Vidéos

```bash
scp ~/Desktop/videos/* gycha@gycha.local:/home/gycha/.media/bloc1/videos/
```

---

### 🔁 Copier dans `bloc2`

#### Images

```bash
scp ~/Desktop/images/* gycha@gycha.local:/home/gycha/.media/bloc2/images/
```

#### Vidéos

```bash
scp ~/Desktop/videos/* gycha@gycha.local:/home/gycha/.media/bloc2/videos/
```

---

### 📁 Copier dans le dossier général (par défaut)

#### Images

```bash
scp ~/Desktop/images/* gycha@gycha.local:/home/gycha/.media/images/
```

#### Vidéos

```bash
scp ~/Desktop/videos/* gycha@gycha.local:/home/gycha/.media/videos/
```

---

## 📦 Copier depuis une clé USB

Si la clé USB est montée sur `/media/gycha/USB`, utiliser :

#### Copier toutes les images

```bash
cp /media/gycha/USB/*.jpg /home/gycha/.media/images/
cp /media/gycha/USB/*.png /home/gycha/.media/images/
```

#### Copier toutes les vidéos

```bash
cp /media/gycha/USB/*.mp4 /home/gycha/.media/videos/
```

---

## 🛠 Modifier le script Python (si besoin)

```bash
nano /home/gycha/.media/media_display.py
```

---

## 🔁 Redémarrer le Raspberry Pi

```bash
sudo reboot
```

---

## 🧹 Supprimer tout le contenu d’un dossier

```bash
cd /chemin/dossier
rm -rf *
```

---

## ✏ Modifier le texte affiché en bas de l’écran

```bash
nano /home/gycha/.media/texte.txt
```

Puis, écris dans ce fichier le texte à afficher.

---
