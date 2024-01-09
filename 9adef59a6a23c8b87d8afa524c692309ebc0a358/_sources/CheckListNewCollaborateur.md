<!--
Author:		    Noa Chouriberry
Date:		    18.12.2023
Description:    check list pour les choses à faire lors de l'accueil d'un nouveau collaborateur
-->

# Check-list ajout d'un nouveau collaborateur correctement

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


<!-- liste à puce html (pastilles enlevées et tailles changées ->> voir style css) -->
<ul class="checklist">
    <!--<li>
        <input type="checkbox" onClick="toggle(this)" />
        <label>Tout cocher</label>
    </li>-->
    <li>
        <input type="checkbox" name="check">
        <label>Création fiche ESSAIM</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Compte Eduvaud</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Compte PaperCut (crédits, code à 6 chiffres envoyé..)</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Ajout du compte eduvaud dans les bons groupes(automatique?)</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Identifiants transmis par le secrétariat?</label>
    </li>
    <li>
        <input type="checkbox" name="check">
        <label>Passage au bureau IT (rdv pour logiciels office etc..)</label>
    </li>
</ul>

<!-- script js pour faire un bouton "tout cocher">
<script>
    function toggle(source) {
        checkboxes = document.getElementsByName('check');
        for (var i = 0, i < checkboxes.length ; i++) {
            checkboxes[i].checked = source.checked;
        }
}
</script>-->

