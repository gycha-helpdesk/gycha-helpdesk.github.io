
# Liste des règles jamf les plus utiles/importantes




# Renommage de postes / AD
sudo jamf policy -event renamecomputerout <br/>
sudo jamf policy -event renamecomputerad  <br/>
sudo jamf policy -event renamecomputerin  



# Drivers des imprimantes

<h3>Canon:</h3>
sudo jamf policy -event adddrivercanon  

<h3>Epson:</h3>
sudo jamf policy -event adddriverepson  

<h3>HP:</h3>
sudo jamf policy -event adddriverhp  

<h3>Konica (nouvelles imprimantes):</h3>
sudo jamf policy -event adddriverkonica  


<h2>Imprimantes par bâtiments</h2>

<h4>FollowMe:</h4>
sudo jamf policy -event addprinterfollowme<br/><br/>

<h3>Bâtiment A:</h3>
A201, A202, A210, A306, A406, A411, A502<br/>
il faut faire la commande addprinter(nom de la salle)<br/>
exemple: sudo jamf policy -event addprintera201

<h3>Bâtiment B: </h3>
B01: <br/>
sudo jamf policy -event addprinterb01et14000<br/>
sudo jamf policy -event addprinterb01hpm750<br/><br/>

Autres salles bâtiment B (b18, b22, b23, b25, b32, b34)<br/>
même principe que le bâtiment a, addprintersalle

<h3>Bâtiment C:</h3>
sudo jamf policy -event addprinterc03<br/>
sudo jamf policy -event addprinterc06<br/>

<h3>Sport:</h3>
sudo jamf policy -event addprinters01<br/>
sudo jamf policy -event addprinters02<br/><br/>


# Pour supprimer les imprimantes d'un poste
sudo jamf policy -event removeprinters

# Installer Microsoft Remote Desktop
sudo jamf policy -event mrd

# Installer Apple Remote Desktop
sudo jamf policy -event ard