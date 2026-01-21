<!--
Auteur : [À compléter]
Date : [À compléter]
Description : Documentation d’utilisation du script Semaine Silence On Lit
-->

# Documentation — Semaine Silence On Lit


> **Objectif** : Automatiser la lecture de fichiers audio (.mp3) à des horaires précis pour l’événement « Silence On Lit ».

## Les scripts pour la semaine « Silence On Lit » sont disponibles sur Teams, dans GychaIT > MAV > Silence on lit.

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
    
---

## Script complet

Voici le script utilisé pour la semaine Silence On Lit :

```python
import os
import time
import subprocess
from datetime import datetime, timedelta

VOLUME = 63

# Régle le volume de sortie du système
def set_volume():
    subprocess.run(["osascript", "-e", f"set volume output volume {VOLUME}"])

# Lance VLC pour lire un fichier MP3
def play_mp3(mp3_file):
    set_volume()
    subprocess.call(["pkill", "VLC"])  # Ferme toute instance VLC en cours d'exécution
    subprocess.Popen([vlc_path, mp3_file])
    print(f"Lecture de {mp3_file} démarrée.")

# Planifie l'exécution de plusieurs musiques avec des dates et heures précises
def schedule_multiple_mp3_playbacks(playback_schedule):
    """
    Planifie la lecture de fichiers MP3 à des dates et heures précises.
    Args:
        playback_schedule: Liste de tuples (fichier_mp3, date, heure)
                          où date est au format "YYYY-MM-DD" et heure au format "HH:MM:SS"
    """
    print("Démarrage de la planification des lectures musicales...")
    print(f"Nombre de fichiers planifiés : {len(playback_schedule)}")
    sorted_schedule = []
    for mp3_file, target_date, target_time in playback_schedule:
        target_datetime = datetime.strptime(f"{target_date} {target_time}", "%Y-%m-%d %H:%M:%S")
        sorted_schedule.append((mp3_file, target_datetime))
    sorted_schedule.sort(key=lambda x: x[1])
    print("\nPlanification triée par ordre chronologique :")
    for i, (mp3_file, target_datetime) in enumerate(sorted_schedule, 1):
        filename = os.path.basename(mp3_file)
        print(f"{i:2d}. {filename} - {target_datetime.strftime('%Y-%m-%d à %H:%M:%S')}")
    print("\n🔄 Démarrage de la surveillance des heures précises...")
    print("⚡ Mode strict : les chansons ne seront jouées qu'à l'heure exacte !")
    played_songs = set()
    last_next_song_display = None
    while True:
        now = datetime.now()
        current_time_str = now.strftime("%Y-%m-%d %H:%M:%S")
        for mp3_file, target_datetime in sorted_schedule:
            filename = os.path.basename(mp3_file)
            target_time_str = target_datetime.strftime("%Y-%m-%d %H:%M:%S")
            schedule_id = f"{mp3_file}_{target_time_str}"
            if current_time_str == target_time_str and schedule_id not in played_songs:
                print(f"\n🎵 HEURE EXACTE ! Lecture de '{filename}' à {current_time_str}")
                play_mp3(mp3_file)
                played_songs.add(schedule_id)
            elif target_datetime < now and schedule_id not in played_songs:
                print(f"⏭️  RATÉ : '{filename}' devait être joué à {target_time_str}")
                played_songs.add(schedule_id)
        if len(played_songs) >= len(sorted_schedule):
            print("\n✅ Toutes les planifications ont été traitées.")
            break
        remaining = len(sorted_schedule) - len(played_songs)
        next_song = None
        next_datetime = None
        for mp3_file, target_datetime in sorted_schedule:
            schedule_id = f"{mp3_file}_{target_datetime.strftime('%Y-%m-%d %H:%M:%S')}"
            if schedule_id not in played_songs and target_datetime > now:
                next_song = os.path.basename(mp3_file)
                next_datetime = target_datetime
                break
        current_display = None
        if next_song and next_datetime:
            time_until_next = (next_datetime - now).total_seconds()
            if time_until_next > 3600:
                time_display = f"dans {time_until_next/3600:.1f}h"
            elif time_until_next > 60:
                time_display = f"dans {time_until_next/60:.1f}min"
            else:
                time_display = f"dans {time_until_next:.0f}s"
            current_display = f"🎵 Prochaine : '{next_song}' le {next_datetime.strftime('%d/%m à %H:%M:%S')} ({time_display}) | Restantes : {remaining}"
        else:
            current_display = f"⏰ Aucune chanson à venir | Restantes : {remaining}"
        if current_display != last_next_song_display:
            print(current_display)
            last_next_song_display = current_display
        time.sleep(1)
    print("\n✅ Planification terminée. Toutes les musiques ont été jouées.")

# Récupère tous les fichiers MP3 dans un dossier
def getMusic(path):
    import re
    def natural_sort_key(filename):
        return [int(text) if text.isdigit() else text.lower() for text in re.split('([0-9]+)', filename)]
    allMp3Files = []
    mp3_files = [f for f in os.listdir(path) if f.endswith('.mp3') and os.path.isfile(os.path.join(path, f))]
    for nom_fichier in sorted(mp3_files, key=natural_sort_key):
        chemin_complet = os.path.join(path, nom_fichier)
        allMp3Files.append(chemin_complet)
    print(f"📁 Fichiers trouvés dans {path}:")
    for i, fichier in enumerate(allMp3Files, 1):
        nom_fichier = os.path.basename(fichier)
        print(f"   {i:2d}. {nom_fichier}")
    return allMp3Files

# Ajoute un intervalle de temps à une heure donnée
def addTime(heure_départ, interval):
    heure_cible_obj = datetime.strptime(heure_départ, "%H:%M:%S")
    interval = interval.split(':')
    nouvelle_heure = heure_cible_obj + timedelta(hours=int(interval[0]), minutes=int(interval[1]), seconds=int(interval[2]))
    return nouvelle_heure.strftime("%H:%M:%S")

# Fonction utilitaire pour créer facilement une planification sur plusieurs jours
def create_daily_schedule(mp3_files, start_date, end_date, daily_times):
    schedule = []
    start_date_obj = datetime.strptime(start_date, "%Y-%m-%d")
    end_date_obj = datetime.strptime(end_date, "%Y-%m-%d")
    current_date = start_date_obj
    file_index = 0
    while current_date <= end_date_obj:
        date_str = current_date.strftime("%Y-%m-%d")
        for time_str in daily_times:
            if file_index < len(mp3_files):
                schedule.append((mp3_files[file_index], date_str, time_str))
                file_index += 1
            else:
                file_index = 0
                schedule.append((mp3_files[file_index], date_str, time_str))
                file_index += 1
        current_date += timedelta(days=1)
    return schedule

# Chemin du dossier musique
folderMusicPath = os.path.expanduser("~/Desktop/musique")

# Récupère tous les fichiers MP3 du dossier
allMp3Files = getMusic(folderMusicPath)

# Liste des planifications avec date et heure précise pour chaque fichier MP3
playback_schedule = [
    (allMp3Files[0], "2025-09-27", "07:35:10"),
    (allMp3Files[1], "2025-09-27", "10:15:10"),
    (allMp3Files[2], "2025-09-27", "11:04:00"),
    (allMp3Files[3], "2025-09-27", "11:10:36"),
    (allMp3Files[4], "2025-09-27", "11:25:00"),
    (allMp3Files[5], "2025-09-28", "10:27:55"),
    (allMp3Files[6], "2025-09-29", "07:32:46"),
    (allMp3Files[7], "2025-09-29", "10:15:10"),
    (allMp3Files[8], "2025-09-29", "10:27:55"),
    (allMp3Files[9], "2025-09-30", "07:40:34"),
    (allMp3Files[10], "2025-09-30", "10:15:10"),
    (allMp3Files[11], "2025-09-30", "10:27:55"),
    (allMp3Files[12], "2025-10-01", "07:33:16"),
    (allMp3Files[13], "2025-10-01", "10:15:10"),
    (allMp3Files[14], "2025-10-01", "10:27:55"),
]

# ⚠️ Il est impératif d'avoir le même nombre de fichiers .mp3 dans le dossier que de lignes dans la planification !
# Par exemple, ici il y a 15 lignes, donc il faut 15 fichiers .mp3 dans le dossier 'musique'.


# Chemin vers VLC (par défaut sur macOS)
vlc_path = "/Applications/VLC.app/Contents/MacOS/VLC"

# Planifie la lecture de la playlist avec dates et heures précises
schedule_multiple_mp3_playbacks(playback_schedule)
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

