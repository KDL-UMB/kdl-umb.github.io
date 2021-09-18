---
layout: page
title: scientific writing
permalink: /tech-writing/
description: Scientific writing example sentences in papers or articles.
nav: true
horizontal: true
---
<div class="projects">
  <!-- Display projects without categories -->
    {% assign sorted_writings = site.tech-writing | sort: "importance" %}
    <!-- Generate cards for each writing -->
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-3">
        {% for writing in sorted_writings %}
          {% include tech_writing.html %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="grid">
        {% for writing in sorted_writings %}
          {% include tech_writing.html %}
        {% endfor %}
      </div>
    {% endif %}

</div>
