---
layout: page
permalink: /publications/
title: Publications
description:
years: [2022,2024]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->

### Preprints

<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f preprints -q @*[year={{y}}]* %}
{% endfor %}

</div>

### Journal articles

<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
