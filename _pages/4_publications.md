---
layout: page
title: publications
permalink: /publications/
description: Peer-reviewed journal articles and book chapters in reverse-chronological order.
---

## Publications

{% assign publications = site.data.publications %}

<div class="publications">
  {% assign years = publications | group_by: "year" | sort: "name" | reverse %}
  {% for year_group in years %}
    <h3 class="year">{{ year_group.name }}</h3>
    {% assign pubs = year_group.items | sort: "title" %}
    {% for pub in pubs %}
    <div class="publication">
      <div class="pub-title">
        {% if pub.url %}
          <a href="{{ pub.url }}" target="_blank">{{ pub.title }}</a>
        {% else %}
          {{ pub.title }}
        {% endif %}
      </div>
      <div class="pub-authors">{{ pub.authors }}</div>
      <div class="pub-journal">
        <em>{{ pub.journal }}</em>{% if pub.volume %}, {{ pub.volume }}{% endif %}{% if pub.number %}({{ pub.number }}){% endif %}{% if pub.pages %}, {{ pub.pages }}{% endif %}{% if pub.doi %}, doi: <a href="https://doi.org/{{ pub.doi }}" target="_blank">{{ pub.doi }}</a>{% endif %}
      </div>
    </div>
    {% endfor %}
  {% endfor %}
</div>
