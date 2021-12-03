---
layout: page
permalink: /members/
title: members
description: members
nav: true
---
<h3 class="mt-4">The University of Massachusetts, Boston</h3>
<div class="projects">
{% assign sorted_teaching = site.teaching | sort: "semester" | reverse %}
{% for teaching in sorted_teaching %}
    {% include teaching.html %}
{% endfor %}
</div>
