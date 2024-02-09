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

    {%- comment -%}  Count bibliography in actual section and year {%- endcomment -%}
    {%- capture citecount -%}
    {%- bibliography_count -f preprints -q @*[year={{y}}]* -%}
    {%- endcapture -%}

    {%- comment -%} If exist bibliography in actual section and year, print {%- endcomment -%}
    {%- if citecount !="0" %}

      <h2 class="year">{{y}}</h2>
    {% bibliography -f preprints -q @*[year={{y}}]* %}

    {%- endif -%}
{% endfor %}

</div>

### Journal articles

<div class="publications">

{%- for y in page.years %}

    {%- comment -%}  Count bibliography in actual section and year {%- endcomment -%}
    {%- capture citecount -%}
    {%- bibliography_count -f papers -q @*[year={{y}}]* -%}
    {%- endcapture -%}

    {%- comment -%} If exist bibliography in actual section and year, print {%- endcomment -%}
    {%- if citecount !="0" %}

      <h2 class="year">{{y}}</h2>
    {% bibliography -f papers -q @*[year={{y}}]* %}

    {%- endif -%}
{% endfor %}

</div>
