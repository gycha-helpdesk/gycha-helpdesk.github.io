
<!--
Author:		    Noa Chouriberry
Date:		    20.09.2023
Description:    check list pour controler la mise en place d'un poste
-->

# Check-list mise en place de poste

<!-- style css des checkbox -->
<style>
    ul.checklist{
        list-style-type: none; font-size: 1.35em; margin-top: 10vh; margin-bottom: 10vh; 
    }
    input[type='checkbox'] {
        transform: scale(1.5);
    }
    ul.checklist li label{
        margin-left: 1vw;
    }
    .margin{
        margin-bottom: 27vh;
    }
</style>

<!-- script js pour faire un bouton "tout cocher">
<script language="JavaScript">
    function toggle(source) {
        checkboxes = document.getElementsByName('check');
        for (var i = 0, i < checkboxes.length ; i++) {
            checkboxes[i].checked = source.checked;
        }
}
</script>-->
<!-- liste à puce html (pastilles enlevées et tailles changées ->> voir style css) -->
<ul class="checklist">
    <!--<li>
        <input type="checkbox" onClick="toggle(this)" />
        <label>Tout cocher</label>
    </li>-->
    <li>
        <input type="checkbox" name="check">
        <label>Clavier/Souris OK</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Session adminl OK</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Session externe (eduvaud) OK</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Bonne version d'OS</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Réseau en .40 OK</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Bon nom</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Profils jamf installés (et EDUVAUD-INTERNE si poste wifi)</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Applications installées (Microsoft 365, Navigateurs, Adobe etc.)</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>WiFi OFF (si c'est un mac mini ou un poste sans wifi)</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Clic droit de la souris activé</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Bonne configuration de recopie vidéo</label>
    </li>
    <li>
        <input type="checkbox" class="margin" name="check">
        <label>Permissions Wacom Confidentialité & sécurité (si mac mini)</label>
    </li>
</ul>

