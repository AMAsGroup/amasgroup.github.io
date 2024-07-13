---
title: "AMAs - Team"
layout: gridlay
excerpt: "AMAs: Team members"
sitemap: false
permalink: /team/
---

# Group Members

 **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**


## Principal Investigator
{% assign number_printed = 0 %}
{% for member in site.data.leader %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="20%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i><br>
  <i>{{ member.institute }}</i>
  <br>Email: <{{ member.email }}>
  <br>
  {%- if member.linkedin -%}
  <a href="https://www.linkedin.com/in/{{ member.linkedin }}" title="Linkedin" target="_blank">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1.5em">
      <i class="fab fa-linkedin fa-stack-1x"></i>
    </span>
    <span class="sr-only">Linkedin</span>
  </a>
  {%- endif -%}

  {%- if member.gscholar -%}
  <a href="https://scholar.google.com/citations?user={{ member.gscholar }}" title="GScholar" target="_blank">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1.5em">
      <i class="fa fa-graduation-cap fa-stack-1x"></i>
    </span>
    <span class="sr-only">GScholar</span>
  </a>
  {%- endif -%}

  {%- if member.orcid -%}
  <a href="https://orcid.org/{{ member.orcid }}" title="Orcid" target="_blank">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1.5em">
      <i class="fab fa-orcid fa-stack-1x"></i>
    </span>
    <span class="sr-only">Orcid</span>
  </a>
  {%- endif -%}
  <br>
  <ul style="overflow: hidden">
  
  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}




## Research Assistants
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i><br>
  {% if member.institute %}
  <i>{{ member.institute }}</i>
  {% endif %}
  Email: <{{ member.email }}>
  <br>
  {%- if member.linkedin -%}
  <a href="https://www.linkedin.com/in/{{ member.linkedin }}" title="Linkedin" target="_blank">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1.5em">
      <i class="fab fa-linkedin fa-stack-1x"></i>
    </span>
    <span class="sr-only">Linkedin</span>
  </a>
  {%- endif -%}

  {%- if member.gscholar -%}
  <a href="https://scholar.google.com/citations?user={{ member.gscholar }}" title="GScholar" target="_blank">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1.5em">
      <i class="fa fa-graduation-cap fa-stack-1x"></i>
    </span>
    <span class="sr-only">GScholar</span>
  </a>
  {%- endif -%}

  {%- if member.orcid -%}
  <a href="https://orcid.org/{{ member.orcid }}" title="Orcid" target="_blank">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1.5em">
      <i class="fab fa-orcid fa-stack-1x"></i>
    </span>
    <span class="sr-only">Orcid</span>
  </a>
  {%- endif -%}
  <br>
  <ul style="overflow: hidden">
  
  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}



## Former BSc/ MSc students
<div class="row">

<div class="col-sm-4 clearfix">
<h4>Doctoral students</h4>
{% for member in site.data.alumni_phd %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Master students</h4>
{% for member in site.data.alumni_msc %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Bachelor Students</h4>
{% for member in site.data.alumni_bsc %}
{{ member.name }}
{% endfor %}
</div>

</div>

<style>
  .fa-stack:hover {
    color: #00002e;
  }
</style>

<!-- ## Administrative Support
<a href="mailto:Rijsewijk@Physics.LeidenUniv.nl">Ellie van Rijsewijk</a> is helping us (and other groups) with administration. -->
