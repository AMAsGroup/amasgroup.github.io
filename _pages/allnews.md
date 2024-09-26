---
title: "News"
layout: textlay
excerpt: "AMAs Group at MERC."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
    <p>{{ article.date }} <br> {{ article.headline }}</p>
{% endfor %}
