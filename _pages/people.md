---
layout: page
title: People
permalink: /people/
description: Including 30+ Faculties, PhDs, Masters, and Undergraduate students.
nav: true
nav_order: 6
display_categories: [Faculties, PhD Students, Master Students, Undergraduate Students]
horizontal: false
---

<!-- pages/peoples.md -->
<div class="peoples">
{%- if page.display_categories %}
  <!-- Display categorized peoples -->
  {%- for category in page.display_categories %}
  <h2 class="category test">{{ category }}</h2>
  {%- assign categorized_peoples = site.people | where: "category", category -%}
  {%- assign sorted_peoples = categorized_peoples | sort: "importance" %}
  <!-- Generate cards for each people -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for people in sorted_peoples -%}
      {% include people_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for people in sorted_peoples -%}
      {% include people.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display peoples without categories -->
  {%- assign sorted_peoples = site.people | sort: "importance" -%}
  <!-- Generate cards for each people -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for people in sorted_peoples -%}
      {% include people_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for people in sorted_peoples -%}
      {% include people.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
