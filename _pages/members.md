---
layout: page
permalink: /members/
title: members
description: members
nav: true
---
<h3 class="mt-4">The University of Massachusetts, Boston</h3>
<div class="projects">
{% assign sorted_members = site.members | sort: "semester" | reverse %}
{% for member in sorted_members %}
    {% include members.html %}
{% endfor %}
</div>
