---
layout: page
title: Deep Dives
permalink: /projects/
description: >
  Longer write-ups on the work of rebuilding Monkey Radio — the sources, the
  consolidation, the hunt, and getting the station back on the air.
sitemap: false
---

Longer write-ups on individual aspects of the rebuild.
{:.lead}

<!-- Grid of image-cards for the `_projects` collection, ordered by each page's
     `order:` front matter. Mirrors the grid on /chasing-the-monkey/. -->
<div class="columns columns-break">
{% assign deep_dives = site.projects | sort: 'order' %}
{% for project in deep_dives %}
  <div class="column column-1-2">
    {% include pro/project-card.html project=project %}
  </div>
{% endfor %}
</div>
