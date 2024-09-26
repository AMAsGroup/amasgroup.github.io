---
title: "News"
layout: textlay
excerpt: "AMAs Group at MERC."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
    <div class="news-item">
        <p><strong>{{ article.date }}</strong><br> {{ article.headline }}</p>
    </div>
{% endfor %}
