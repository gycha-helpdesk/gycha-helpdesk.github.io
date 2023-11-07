<!--
Author:		    Noa Chouriberry
Date:		    20.09.2023
Description:    check list pour controler la mise en place d'un poste
-->

# Checklist configuration Apple TV

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
        <label>AppleTV avec le bon nom (nom de la salle)</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Réseau GYCHA-MAITRES (compte profun.test)</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>AirPlay activé</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Mode salle de conférence > exiger un code à chaque fois</label>
    </li>
</ul>


