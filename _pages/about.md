---
permalink: /
title: "Huiyuan Wang"
excerpt: "Huiyuan Wang"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<div class="home-page">
  <section class="home-intro" aria-labelledby="home-intro-title">
    <p class="home-intro__eyebrow" id="home-intro-title">Research Associate in Biostatistics &middot; University of Pennsylvania</p>
    <p class="home-intro__lead">I develop statistical methods for reliable learning and inference when data are biased, imperfect, distributed, or structurally complex.</p>
    <p>My research spans causal inference and real-world evidence, distributed inference, statistical foundations for adaptive and verifiable AI, and learning from structured data. I am also interested in active learning, retrieval-augmented systems, benchmarking and evaluation of large language models, continual learning, and shortcut-resistant learning.</p>
    <nav class="home-links" aria-label="Profile links">
      <a href="/research/">Research <span aria-hidden="true">&rarr;</span></a>
      <a href="/publications/">Publications <span aria-hidden="true">&rarr;</span></a>
      <a href="/files/cv_huiyuan.pdf">CV (PDF) <span aria-hidden="true">&nearr;</span></a>
      <a href="{{ site.author.googlescholar }}">Google Scholar <span aria-hidden="true">&nearr;</span></a>
      <a href="https://www.mathgenealogy.org/id.php?id=326702">Mathematics Genealogy <span aria-hidden="true">&nearr;</span></a>
      <a href="mailto:huiyuanw@upenn.edu">Email <span aria-hidden="true">&nearr;</span></a>
    </nav>
  </section>

  <section class="home-news" aria-labelledby="news-title">
    <div class="home-section-heading">
      <h2 id="news-title">News</h2>
      <span>Selected updates</span>
    </div>
    <ol class="home-news__list">
      {% for item in site.data.news %}
        <li class="home-news__item">
          <time>{{ item.date }}</time>
          <div>
            <div class="home-news__headline">
              {% if item.label %}<span class="home-news__tag">{{ item.label }}</span>{% endif %}
              {% if item.url %}
                <a href="{{ item.url }}">{{ item.title }} <span aria-hidden="true">&nearr;</span></a>
              {% else %}
                <strong>{{ item.title }}</strong>
              {% endif %}
            </div>
            {% if item.description %}<p>{{ item.description }}</p>{% endif %}
          </div>
        </li>
      {% endfor %}
    </ol>
  </section>
</div>
