---
layout: page
title: members
permalink: /members/
description: All Members work on KD Lab
nav: true
display_categories: [work, fun]
horizontal: true
---
<div class="projects">
    <h1> Current PhD Students </h1>
  <!-- Display projects without categories -->
    {% assign sorted_projects = site.members | sort: "importance" | reverse%}
    <!-- Generate cards for each project -->
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-1">
        {% for project in sorted_projects %}
          {% include projects_horizontal.html %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="grid">
        {% for project in sorted_projects %}
          {% include projects.html %}
        {% endfor %}
      </div>
    {% endif %}
    
    <h1> Former PhD Students </h1>
    {% assign sorted_projects = site.members | sort: "importance" | reverse%}
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-3">
        {% for project in sorted_projects %}
          {% include projects_horizontal2.html %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="grid">
        {% for project in sorted_projects %}
          {% include projects.html %}
        {% endfor %}
      </div>
    {% endif %}


</div>