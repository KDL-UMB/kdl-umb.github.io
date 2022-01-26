---
layout: page
title: meeting
permalink: /meeting/
description: Weekly meeting for students to share their weekly work and discuss with team members.
nav: false
horizontal: true
---
<div class="projects">
  <!-- Display projects without categories -->
    {% assign sorted_writings = site.meeting | sort: "title" | reverse %}
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