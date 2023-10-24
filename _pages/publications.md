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
    onclick="changeBibliography('physRevBib')">
        ML system
    </button>
    <div id="defaultBib" style="display:block;">
        {% bibliography -f {{ site.scholar.bibliography_default }} %}
    </div>
    <div id="dataCentricBib" style="display:none;">
        {% bibliography -f {{ site.scholar.bibliography_dataCentric }} %}
    </div>
    <div id="physRevBib" style="display:none;">
        {% bibliography -f {{ site.scholar.bibliography_physRev }} %}
    </div>
</div>

<script>
    var button_choice = 'defaultBib';
    function changeBibliography(choice) {
        // 根据需要修改 site.scholar.bibliography 的值
        if (choice === 'dataCentricBib') {
            document.getElementById("dataCentricBib").style.display = "block"; // 显示选中元素
            // 其余均隐藏
            document.getElementById("defaultBib").style.display = "none";
            document.getElementById("physRevBib").style.display = "none";
        } else if (choice === 'physRevBib') {
            document.getElementById("physRevBib").style.display = "block"; // 显示选中元素
            // 其余均隐藏
            document.getElementById("defaultBib").style.display = "none";
            document.getElementById("dataCentricBib").style.display = "none";
        } else { // defaultBib
            document.getElementById("defaultBib").style.display = "block"; // 显示选中元素
            // 其余均隐藏
            document.getElementById("physRevBib").style.display = "none";
            document.getElementById("dataCentricBib").style.display = "none";
        }
    }
</script>
