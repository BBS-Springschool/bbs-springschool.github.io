---
title: "BBS Springschool"
layout: gridlay
excerpt: "Organizing team"
sitemap: false
permalink: /team/
---

# Committee

{% assign number_printed = 0 %}
{% for member in site.data.committee %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img id="{{ member.lastname }}" src="{{ site.url }}{{ site.baseurl }}/images/committee_pic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.firstname }} {{ member.lastname }}</h4>
  <i> {{ member.role }}<br>
      {{ member.university }}<br>
      {{ member.department }}<br>
      email: {{ member.email }}
  </i>
  <ul class="no-bullets" style="overflow: hidden">

  {% if member.number_info == 1 %}
  <li> {{ member.info1 }} </li>
  {% endif %}

  {% if member.number_info == 2 %}
  <li> {{ member.info1 }} </li>
  <li> {{ member.info2 }} </li>
  {% endif %}

  {% if member.number_info == 3 %}
  <li> {{ member.info1 }} </li>
  <li> {{ member.info2 }} </li>
  <li> {{ member.info3 }} </li>
  {% endif %}

  {% if member.number_info == 4 %}
  <li> {{ member.info1 }} </li>
  <li> {{ member.info2 }} </li>
  <li> {{ member.info3 }} </li>
  <li> {{ member.info4 }} </li>
  {% endif %}

  {% if member.number_info == 5 %}
  <li> {{ member.info1 }} </li>
  <li> {{ member.info2 }} </li>
  <li> {{ member.info3 }} </li>
  <li> {{ member.info4 }} </li>
  <li> {{ member.info5 }} </li>
  {% endif %}
  {% if member.url %}
  <li> <a href="{{ member.url }}">See webpage</a></li>
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



