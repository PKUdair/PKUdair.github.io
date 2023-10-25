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
    <button style="display: inline-block; background-color: #ffdead; color: #FFFFFF; border-radius: 5px; outline: none;" 
    onclick="changeBibliography('GraphMLBib')">
        Graph ML
    </button>
    <button style="display: inline-block; background-color: #e6e6fa; color: #FFFFFF; border-radius: 5px; outline: none;" 
    onclick="changeBibliography('AI4scienceBib')">
        AI4science
    </button>
    <button style="display: inline-block; background-color: #98fb98; color: #FFFFFF; border-radius: 5px; outline: none;" 
    onclick="changeBibliography('AI4industryBib')">
        AI4industry
    </button>
    <button style="display: inline-block; background-color: #ffe1ff; color: #FFFFFF; border-radius: 5px; outline: none;" 
    onclick="changeBibliography('DatabaseBib')">
        Database
    </button>
    <button style="display: inline-block; background-color: #cd0000; color: #FFFFFF; border-radius: 5px; outline: none;" 
    onclick="changeBibliography('AutoMLBib')">
        AutoML
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
    <div id="GraphMLBib" style="display:none;">
        {% bibliography -f {{ site.scholar.bibliography_GraphML }} %}
    </div>
    <div id="AI4scienceBib" style="display:none;">
        {% bibliography -f {{ site.scholar.bibliography_AI4science }} %}
    </div>
    <div id="AI4industryBib" style="display:none;">
        {% bibliography -f {{ site.scholar.bibliography_AI4industry }} %}
    </div>
    <div id="DatabaseBib" style="display:none;">
        {% bibliography -f {{ site.scholar.bibliography_Database }} %}
    </div>
    <div id="AutoMLBib" style="display:none;">
        {% bibliography -f {{ site.scholar.bibliography_AutoML }} %}
    </div>
</div>

<script>
    var button_choice = 'defaultBib';
    function changeBibliography(choice) {
        if (choice === 'dataCentricBib') {
            document.getElementById("dataCentricBib").style.display = "block"; // 显示选中元素
            // 其余均隐藏
            document.getElementById("defaultBib").style.display = "none";
            document.getElementById("MLsystemBib").style.display = "none";
            document.getElementById("GraphMLBib").style.display = "none";
            document.getElementById("AI4scienceBib").style.display = "none";
            document.getElementById("AI4industryBib").style.display = "none";
            document.getElementById("DatabaseBib").style.display = "none";
            document.getElementById("AutoMLBib").style.display = "none";
        } else if (choice === 'MLsystemBib') {
            document.getElementById("MLsystemBib").style.display = "block"; // 显示选中元素
            // 其余均隐藏
            document.getElementById("defaultBib").style.display = "none";
            document.getElementById("dataCentricBib").style.display = "none"; 
            document.getElementById("GraphMLBib").style.display = "none";
            document.getElementById("AI4scienceBib").style.display = "none";
            document.getElementById("AI4industryBib").style.display = "none";
            document.getElementById("DatabaseBib").style.display = "none";
            document.getElementById("AutoMLBib").style.display = "none";
        } else if (choice === 'GraphMLBib') {
            document.getElementById("GraphMLBib").style.display = "block"; // 显示选中元素
            // 其余均隐藏
            document.getElementById("defaultBib").style.display = "none";
            document.getElementById("dataCentricBib").style.display = "none"; 
            document.getElementById("MLsystemBib").style.display = "none";
            document.getElementById("AI4scienceBib").style.display = "none";
            document.getElementById("AI4industryBib").style.display = "none";
            document.getElementById("DatabaseBib").style.display = "none";
            document.getElementById("AutoMLBib").style.display = "none";
        } else if (choice === 'AI4scienceBib') {
            document.getElementById("AI4scienceBib").style.display = "block"; // 显示选中元素
            // 其余均隐藏
            document.getElementById("defaultBib").style.display = "none";
            document.getElementById("dataCentricBib").style.display = "none"; 
            document.getElementById("GraphMLBib").style.display = "none";
            document.getElementById("MLsystemBib").style.display = "none";
            document.getElementById("AI4industryBib").style.display = "none";
            document.getElementById("DatabaseBib").style.display = "none";
            document.getElementById("AutoMLBib").style.display = "none";
        } else if (choice === 'AI4industryBib') {
            document.getElementById("AI4industryBib").style.display = "block"; // 显示选中元素
            // 其余均隐藏
            document.getElementById("defaultBib").style.display = "none";
            document.getElementById("dataCentricBib").style.display = "none"; 
            document.getElementById("GraphMLBib").style.display = "none";
            document.getElementById("AI4scienceBib").style.display = "none";
            document.getElementById("MLsystemBib").style.display = "none";
            document.getElementById("DatabaseBib").style.display = "none";
            document.getElementById("AutoMLBib").style.display = "none";
        } else if (choice === 'DatabaseBib') {
            document.getElementById("DatabaseBib").style.display = "block"; // 显示选中元素
            // 其余均隐藏
            document.getElementById("defaultBib").style.display = "none";
            document.getElementById("dataCentricBib").style.display = "none"; 
            document.getElementById("GraphMLBib").style.display = "none";
            document.getElementById("AI4scienceBib").style.display = "none";
            document.getElementById("AI4industryBib").style.display = "none";
            document.getElementById("MLsystemBib").style.display = "none";
            document.getElementById("AutoMLBib").style.display = "none";
        } else if (choice === 'AutoMLBib') {
            document.getElementById("AutoMLBib").style.display = "block"; // 显示选中元素
            // 其余均隐藏
            document.getElementById("defaultBib").style.display = "none";
            document.getElementById("dataCentricBib").style.display = "none"; 
            document.getElementById("GraphMLBib").style.display = "none";
            document.getElementById("AI4scienceBib").style.display = "none";
            document.getElementById("AI4industryBib").style.display = "none";
            document.getElementById("DatabaseBib").style.display = "none";
            document.getElementById("MLsystemBib").style.display = "none";
        } else { // defaultBib
            document.getElementById("defaultBib").style.display = "block"; // 显示选中元素
            // 其余均隐藏
            document.getElementById("AutoMLBib").style.display = "none";
            document.getElementById("dataCentricBib").style.display = "none"; 
            document.getElementById("GraphMLBib").style.display = "none";
            document.getElementById("AI4scienceBib").style.display = "none";
            document.getElementById("AI4industryBib").style.display = "none";
            document.getElementById("DatabaseBib").style.display = "none";
            document.getElementById("MLsystemBib").style.display = "none";
        }
    }
</script>
