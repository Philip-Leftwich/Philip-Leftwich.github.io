---
layout: archive
title: "People"
permalink: /people/
author_profile: true
---

{% for post in site.people reversed %}
  {% if post.categories contains "past" %}
    <h2>Past</h2>
    {% include archive-single.html %}
  {% elsif post.categories contains "present" %}
    <h2>Present</h2>
    {% include archive-single.html %}
  {% endif %}
{% endfor %}




Collaborators
======
[Professor Tracey Chapman](https://www.traceychapmanresearch.com/)

[Professor Luke Alphey](https://www.pirbright.ac.uk/users/prof-luke-alphey)
