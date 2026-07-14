---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<div class="publications-list">
  <div class="publications-list__intro">
    <a class="profile-link" href="{{ site.author.googlescholar }}">Google Scholar <span aria-hidden="true">&nearr;</span></a>
    <span><sup>*</sup> Equal contribution.</span>
  </div>

  {% assign published_papers = site.publications | where: "status", "published" | sort: "date" | reverse %}
  {% assign publication_years = "2026,2025,2024,2023,2022" | split: "," %}

  {% for year in publication_years %}
    <section class="publication-year-group" aria-labelledby="year-{{ year }}">
      <h2 id="year-{{ year }}" class="publication-year">{{ year }}</h2>
      <ol class="publication-year__items">
        {% for post in published_papers %}
          {% assign paper_year = post.date | date: "%Y" %}
          {% if paper_year == year %}
            {% include publication-compact.html %}
          {% endif %}
        {% endfor %}
      </ol>
    </section>
  {% endfor %}
</div>
