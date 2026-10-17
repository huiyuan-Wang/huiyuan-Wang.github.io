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

  {% assign published_papers = site.publications | where: "status", "published" %}
  {% assign accepted_papers = site.publications | where: "status", "accepted" %}
  {% assign revision_papers = site.publications | where: "status", "under-revision" %}
  {% assign listed_papers = published_papers | concat: accepted_papers | concat: revision_papers | sort: "date" | reverse %}
  {% assign publication_years = "2026,2025,2024,2023,2022" | split: "," %}

  {% for year in publication_years %}
    <section class="publication-year-group" aria-labelledby="year-{{ year }}">
      <h2 id="year-{{ year }}" class="publication-year">{{ year }}</h2>
      <ol class="publication-year__items">
        {% for post in listed_papers %}
          {% assign paper_year = post.date | date: "%Y" %}
          {% assign has_public_version = false %}
          {% if post.status == "published" and post.paperurl %}
            {% assign has_public_version = true %}
          {% elsif post.status == "accepted" and post.public_listing_authorized %}
            {% assign has_public_version = true %}
          {% elsif post.public_source_verified and post.public_source_type == "arxiv" and post.paperurl contains "https://arxiv.org/abs/" %}
            {% assign has_public_version = true %}
          {% elsif post.public_source_verified and post.public_source_type == "publisher" and post.paperurl %}
            {% assign has_public_version = true %}
          {% endif %}
          {% if paper_year == year and has_public_version %}
            {% include publication-compact.html %}
          {% endif %}
        {% endfor %}
      </ol>
    </section>
  {% endfor %}
</div>
