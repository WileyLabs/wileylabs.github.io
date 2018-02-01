---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
title: Welcome to WileyLabs
---

{% include epubcheck-message.html %}

We're just getting started, but we'd love your contributions on any of the
projects below.

{% assign projects = site.data.repos | where: "fork","false" %}
<div class="ui cards">
{% for project in projects %}
  {% unless project.name contains 'github.io' %}
    {% unless project.topics contains 'experiment' %}
      {% unless project.topics contains 'meetup' %}
        {% include project-card.html %}
      {% endunless %}
    {% endunless %}
  {% endunless %}
{% endfor %}
</div>

## Experimental Projects

Just a few things we're exploring. Feel free to watch, contribute, or fork!
{% assign projects = site.data.repos | where: "fork","false" | where: "topics", "experiment" %}
{% include project-cards.html %}
