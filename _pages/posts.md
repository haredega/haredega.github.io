---
title: "Posts"
layout: archive
author_profile: true
permalink: /posts/
sitemap: false
excerpt: "This is my spot. But you still can stay around and take a look on what I've been up to. Watch out for some random logorrhoea"
author_profile: true
---

{% include base_path %}

<h3 class="archive__subtitle">{{ site.data.ui-text[site.locale].recent_posts }}</h3>

{% for post in paginator.posts %}
  {% include archive-single.html %}
{% endfor %}

{% include paginator.html %}
