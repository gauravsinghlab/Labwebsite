---
layout: default
title: Publications
description: Selected publications from the GS Research Group.
permalink: /publications/
---

<section class="page-hero">
  <div class="wrap members-intro publications-intro">
    <h1>Publications (<a href="https://scholar.google.com/citations?user=iq-O6EwAAAAJ&amp;hl=en&amp;authuser=3" rel="noreferrer">Google Scholar</a>, # indicates co-corresponding author)</h1>
  </div>
</section>

<section class="wrap publications-list">
  {% for group in site.data.publications %}
    <h2 class="year-heading">{{ group.year }}</h2>
    <div class="pub-list">
      {% for publication in group.items %}
        <article class="publication-card">
          <h3>
            {% if publication.url %}
              <a href="{{ publication.url }}" rel="noreferrer">{{ publication.title }}</a>
            {% else %}
              {{ publication.title }}
            {% endif %}
          </h3>
          <p class="meta">
            <span class="authors">{{ publication.authors }}</span>
            <span class="journal">{{ publication.journal }}</span>
            {% if publication.details %}<span class="details">{{ publication.details }}</span>{% endif %}
          </p>
        </article>
      {% endfor %}
    </div>
  {% endfor %}
</section>
