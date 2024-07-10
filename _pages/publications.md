---
title: "AMAs - Publications"
layout: gridlay
excerpt: "AMAs -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

**For a full list of publications, please refer to the list below or visit <a href="https://scholar.google.com/citations?user=tY66SMIAAAAJ&hl" target="_blank">Google Scholar</a>**

## Highlights

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}" target="_blank">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Full List of publications

{% assign sorted_publist = site.data.publist | sort: 'year' | reverse %}
{% assign current_year = '' %}
{% assign grouped_before_2017 = false %}

{% for publi in sorted_publist %}
  {% if publi.year <= 2017 %}
    {% if grouped_before_2017 == false %}
      {% assign grouped_before_2017 = true %}
      {% if current_year != '' %}
---

      {% endif %}
### 2017 and before
    {% endif %}
  {% else %}
    {% if current_year != publi.year %}
      {% assign current_year = publi.year %}
      {% if forloop.index > 1 %}
---

      {% endif %}
### {{ current_year }}
    {% endif %}
  {% endif %}
  {{ publi.title }}  
  *{{ publi.authors }}*  
  <a href="{{ publi.link.url }}" target="_blank">{{ publi.link.display }}</a>
{% endfor %}