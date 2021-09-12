---
layout: page
permalink: /publications/
title: publications
description: An up-to-date list is available on Google Scholar.
years: [2016, 2017, 2018, 2021]
nav: true
---

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
