---
layout: archive
title: "Presentations"
permalink: /presentations/
author_profile: true
---

{% assign talks = site.talks | sort: "date" | reverse %}

{% for post in talks %}
  <p>
    <strong>{{ post.author}}</strong>
    <strong>{{ post.title }}</strong>
    {% if post.type %}, {{ post.type }}{% endif %}
    {% if post.venue %}, {{ post.venue }}{% endif %}
    {% if post.date %}, {{ post.date | date: "%Y" }}{% endif %}.
    {% if post.slides %}<a href="{{ post.slides }}">Slides</a>{% endif %}
    {% if post.paper %} · <a href="{{ post.paper }}">Paper</a>{% endif %}
    {% if post.video %} · <a href="{{ post.video }}">Video</a>{% endif %}
  </p>
{% endfor %}
