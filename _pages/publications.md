---
title: "AMAs - Publications"
layout: gridlay
excerpt: "AMAs -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

**For a full list of publications, please refer to the list below or visit [Google Scholar](https://scholar.google.com/citations?user=tY66SMIAAAAJ&hl)**

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
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
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
  {% if publi.year <= 2017 and not grouped_before_2017 %}
    {% assign grouped_before_2017 = true %}
    {% if current_year != '' %}
---
    {% endif %}
### 2017 and before
  {% elsif current_year != publi.year and publi.year > 2017 %}
    {% assign current_year = publi.year %}
    {% if forloop.index > 1 %}

---
    {% endif %}
### {{ current_year }}
  {% endif %}
  {{ publi.title }}  
  *{{ publi.authors }}*  
  [{{ publi.link.display }}]({{ publi.link.url }})
{% endfor %}