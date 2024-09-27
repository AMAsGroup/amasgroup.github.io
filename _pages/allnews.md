---
title: "News"
layout: textlay
excerpt: "AMAs Group at MERC."
sitemap: false
permalink: /allnews.html
---

<!-- # News

{% for article in site.data.news %}
    {{ article.date }}
    {{ article.headline }}
{% endfor %} -->
<div class="well">
    <h4>News</h4>

    {% for article in site.data.news %}
    <p>{{ article.date }}<br>{{ article.headline | markdownify}}</p>
    {% endfor %}
</div>