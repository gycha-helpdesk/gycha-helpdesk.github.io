<!--
Auteur : [Maxence]
Date : [24.02.2026]
Description : Régler le problème de code de sortie 17 du logiciel Thonny.
-->

# Résoudre l'Erreur "Code de sortie 17" sur macOS

Si en utilisant **Thonny** sur un Mac s'affiche le message `Process ended with exit code 17`, c'est généralement parce que le logiciel n'a plus l'autorisation d'accéder à vos dossiers système (Documents, Bureau, etc.).

C'est un problème fréquent qui survient lorsqu'on refuse par mégarde la demande de permission de macOS lors du premier lancement.

---

## 🛠 Procédure de réparation

Suivez ces étapes pour restaurer les droits d'accès de Thonny :

### 1. Ouvrir les réglages système
1. Cliquez sur le menu **Pomme ()** en haut à gauche.
2. Choisissez **Réglages Système** (ou *Préférences Système*).
3. Dans la barre latérale, cliquez sur **Confidentialité et sécurité**.

### 2. Accorder l'accès au répertoire
C'est la méthode la plus fiable pour éviter que l'erreur ne revienne.

1. Dans la liste de droite, faites défiler jusqu'à **Accès Fichiers et dossiers**.
2. Cherchez **Thonny** dans la liste des applications.
3. **Activez l'interrupteur** du répertoire voulu que ça soit Documents ou OneDrive(il doit devenir bleu). 
   * *Note : Vous devrez probablement saisir le mot de passe de session admin.*