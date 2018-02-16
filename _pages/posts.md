---
title: "Posts"
layout: archive
author_profile: true
permalink: /posts/
sitemap: false
excerpt: "This is my spot. But you still can stay around and take a look on what I've been up to. Watch out for some random logorrhoea"
author_profile: true
---

{% assign postsByYear = site.posts | group_by_exp:"post", "post.date | date: '%Y'"  %}
{% for year in postsByYear %}
  <h2 id="{{ year.name | slugify }}" class="archive__subtitle">{{ year.name }}</h2>
  {% for post in year.items %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
