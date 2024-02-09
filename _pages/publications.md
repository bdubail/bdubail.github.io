---
layout: page
permalink: /publications/
title: Publications
description:
sections:
  - type: "ARXIV"
    text: "Preprints"
  - type: "JOUR"
    text: "Journal articles"
  - type: "@inproceedings"
    text: "Conference and workshop papers"
  - type: "@misc|@phdthesis|@mastersthesis"
    text: "Thesis"
years: [2022,2024]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->

### Preprints

<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[TY={{ARXIV},year={{y}}]* %}
{% endfor %}

</div>

### Journal articles

<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[TY={{JOUR}},year={{y}}]* %}
{% endfor %}

</div>
