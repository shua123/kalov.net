---
layout: default
title: Speaking
permalink: /speaking/
list_title: 
---

# {{ page.title }}

{% assign sorted = site.data.events | sort: 'date' | reverse %}
<ul>
{% for event in sorted %}
  <li>{{ event.date | date: "%m/%d/%Y" }} {% if event.event_link %}<a href="{{ event.event_link }}" target="_blank">{{ event.event }}</a>{% else %}{{ event.event }}{% endif %} {% if event.title %}- {{ event.title }}{% endif %}{% if event.description %}: <i>{{ event.description }}</i>{% endif %}{% if event.slides_link %} <a href="{{ event.slides_link }}" target="_blank" title="{{ event.event }} Slides">Slides</a>{% endif %}
  </li>
{% endfor %}
</ul>