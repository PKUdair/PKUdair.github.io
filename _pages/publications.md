---
layout: page
permalink: /publications/
title: Publications
description: 
nav: true
nav_order: 7
---
<!-- _pages/publications.md -->
<div class="publications">
    <!-- <div>machine learning</div> -->
    <button style="display: inline-block; background-color: #6A7689; color: #FFFFFF; border-radius: 5px; outline: none;" 
    onclick="changeBibliography('defaultBib')">
        Default
    </button>
    <button style="display: inline-block; background-color: #89009F; color: #FFFFFF; border-radius: 5px; outline: none;" 
    onclick="changeBibliography('dataCentricBib')">
        Data-centric ML
    </button>
    <button style="display: inline-block; background-color: #00369f; color: #FFFFFF; border-radius: 5px; outline: none;" 
    onclick="changeBibliography('MLsystemBib')">
        ML system
    </button>
    <button style="display: inline-block; background-color: #e6e6fa; color: #FFFFFF; border-radius: 5px; outline: none;" 
    onclick="changeBibliography('DatabaseBib')">
        Database
    </button>
    <button style="display: inline-block; background-color: #cd0000; color: #FFFFFF; border-radius: 5px; outline: none;" 
    onclick="changeBibliography('AutoMLBib')">
        AutoML
    </button>
    <button style="display: inline-block; background-color: #ffdead; color: #FFFFFF; border-radius: 5px; outline: none;" 
    onclick="changeBibliography('OthersBib')">
        Others
    </button>
    
    <div id="defaultBib" style="display:block;">
        {% bibliography -f {{ site.scholar.bibliography_default }} %}
    </div>
    <div id="dataCentricBib" style="display:none;">
        {% bibliography -f {{ site.scholar.bibliography_dataCentric }} %}
    </div>
    <div id="MLsystemBib" style="display:none;">
        {% bibliography -f {{ site.scholar.bibliography_MLsystem }} %}
    </div>
    <div id="DatabaseBib" style="display:none;">
        {% bibliography -f {{ site.scholar.bibliography_Database }} %}
    </div>
    <div id="AutoMLBib" style="display:none;">
        {% bibliography -f {{ site.scholar.bibliography_AutoML }} %}
    </div>
    <div id="OthersBib" style="display:none;">
        {% bibliography -f {{ site.scholar.bibliography_Others }} %}
    </div>
</div>

<script>
    function changeBibliography(choice) {
        document.getElementById("defaultBib").style.display = "none";
        document.getElementById("dataCentricBib").style.display = "none";
        document.getElementById("MLsystemBib").style.display = "none";
        document.getElementById("DatabaseBib").style.display = "none";
        document.getElementById("AutoMLBib").style.display = "none";
        document.getElementById("OthersBib").style.display = "none";

        document.getElementById(choice).style.display = "block";
    }
</script>
