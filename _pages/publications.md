---
layout: page
permalink: /publications/
title: Publications
description:
sections:
  - bibquery: "@article"
    text: "Journal articles"
  - bibquery: "@inproceedings"
    text: "Conference and workshop papers"
  - bibquery: "@misc|@phdthesis|@mastersthesis"
    text: "Thesis"
years: [2022,2024]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->

<div class="publications">

{%- for section in ["JOUR","ARXIV"] %}
  <a id="{{section}}"></a>
  <p class="bibtitle">{{section}}</p>
  {%- for y in page.years %}

    {%- comment -%}  Count bibliography in actual section and year {%- endcomment -%}
    {%- capture citecount -%}
    {%- bibliography_count -f papers -q @*[TY={{section}},year={{y}}]* -%}
    {%- endcapture -%}

    {%- comment -%} If exist bibliography in actual section and year, print {%- endcomment -%}
    {%- if citecount !="0" %}

      <h2 class="year">{{y}}</h2>
      {% bibliography -f papers -q @*[TY={{section},year={{y}}]* %}

    {%- endif -%}

  {%- endfor %}

{%- endfor %}

</div>
