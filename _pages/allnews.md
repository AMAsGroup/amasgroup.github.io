---
title: "News"
layout: textlay
excerpt: "AMAs Group at MERC."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
{{ article.date }}<br>
<i>{{ article.headline | markdownify}}</i>
{% endfor %}
