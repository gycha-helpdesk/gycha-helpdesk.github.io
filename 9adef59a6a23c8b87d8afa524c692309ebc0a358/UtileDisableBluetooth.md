# Désactiver complètement le bluetooth d'un poste

Pour commencer, il faut démarrer l'ordinateur en mode récupration (laisser appuyer cmd+r au démarrage) 
Après il faut aller dans Utilitaires > Terminal et taper la commande suivante:
```
csrutil disable
```
Cette commande sert à désactiver la protection d'intégrité système, ce qui nous permettera de désactiver le bluetooth par la suite.
Dés que c'est fait, vous pouvez redémarrer l'ordinateur normalement et mettre les identifiants admin.
Après, il faut aller dans les paramètres du mac et désactiver le bluetooth:

```{image} images/disableBluetooth.png
:width: 500px
:name: disableBluetooth.png
:align: center
```

Puis ouvrir un terminal et taper la commande suivante:
```
sudo launchctl unload -w /System/Library/LaunchDaemons/com.apple.bluetoothd.plist
```
Ensuite, il faut redémarrer le poste et appuyer sur cmd+r pour aller en mode récupération une nouvelle fois et donc réactiver la protection d'intégrité système. 
Il faut ouvrir un terminal et faire la commande csrutil enable.




redémarrer

pour réactiver le bluetooth: 
sudo launchctl load -w /System/Library/LaunchDaemons/com.apple.bluetoothd.plist
sudo defaults write /Library/Preferences/com.apple.Bluetooth ControllerPowerState -int 1

redémarrer avec cmd+r 
terminal > csrutil enable

redémarrer
