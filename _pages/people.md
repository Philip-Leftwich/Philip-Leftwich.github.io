---
layout: archive
title: "People"
permalink: /people/
author_profile: true
---

{% for post in site.people reversed %}
  {% if post.categories contains "past" %}
    <h1>Past</h1>
    {% include archive-single.html %}
  {% elsif post.categories contains "present" %}
    <h1>Present</h1>
    {% include archive-single.html %}
  {% endif %}
{% endfor %}




Collaborators
======
[Professor Tracey Chapman](https://www.traceychapmanresearch.com/)

[Professor Luke Alphey](https://www.pirbright.ac.uk/users/prof-luke-alphey)
