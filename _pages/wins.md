---
layout: page
title: women in science
permalink: /wins/
description: The purpose of this Club is to create a supportive community of faculty and students where students can discuss issues related to women in STEM fields, barriers women face, and strategies to overcome these barriers. Champion young women to advance in a STEM field career in and outside of academia. 
nav: false
display_categories: [seminar, fun]
---

<div class="wins">
  <ul class="wins-list">
    {% assign sorted_wins = site.wins | sort: "date" | reverse %}
    {% for wins in sorted_wins %}
      <li>
        <h3><a class="post-title" href="{{ wins.url | prepend: site.baseurl }}">{{ wins.title }}</a></h3>
        <p class="post-meta">{{ wins.date | date: '%B %-d, %Y' }}</p>
        <p>{{ wins.description }}</p>
      </li>
    {% endfor %}
  </ul>

  {% include pagination.html %}
</div>

