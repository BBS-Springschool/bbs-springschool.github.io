---
title: "BBS Springschool"
layout: gridlay
excerpt: "All about the BBS"
sitemap: false
permalink: /about/
---

**“Brain / Behaviour / Society Springschool”** represents a collaborative workshop that tries to combine elements of Hackathons, Unconferences and Educationals. For this school we took the ideas and concepts of [BrainHack](https:/brainhack.org) and now we want to extend it to all scientific disciplines within the field of neuroscience, cognitive science, biology, psychology and social sciences to name only few. Together, we want to bring scientists of all faculties together to work on one goal together. This common goal represents the respective topic of the Brain / Behaviour / Society Springschool.  

This 2022 edition marks the of the **“Brain / Behaviour / Society Spring School”** we hope to settle the starting point for a possible future series of variant themes and topics. 

These collaborative workshops combine elements of Hackathons and Unconferences, with a variety of educational activities, to accelerate the adaptation of data science and computational methods in Neuroscience. Much of the conference is allocated to open working time during which attendees are encouraged to work together in interdisciplinary teams on projects that utilize computational techniques to solve problems in neuroscience. Periodic unconference sessions provide an opportunity for attendees to share their expertise on topics that become relevant through the course of the event. In parallel to these activities, an educational track provide hands-on tutorials on relevant tools such as python, github, cloud computing, and innovative statistical methods.

Following the tradition of open science and joint workshops, we want to revive the the concept of *Springschools*, combine it with the spirit of *[Brainhacks](https://brainhack.org/)* and open it to all interested students to bridge all scientific disciplines. This school aims at combining ideas of a traditional hackathon with educational elements and dedicated thematic talks. 

As such, we plan to combine open-hacking and unconference sessions with a learning track intermixed with featured talks unter the umbrella of a general topic: **“CHANGE: How to measure, detect, and quantify change reliably.”** This topic is inspired by the CoVID-pandemic that consistently changed the world, science, and society. Therefore, all featured talks will be given by invited speakers to enlighten the global theme of **“Change”** either from the perspective of the *brain*, or from the point of view of *behaviour*, or from a *social* point of view. 

With this 2022 edition of the **“Brain / Behaviour / Society Spring School”** we hope to settle the starting point for a possible future series of variant themes and topics. 

We are grateful for the support and funding from the [University of Graz](https://www.uni-graz.at), the [Complexity of LIfe in Basic Research and Innovation (COLIBRI)](https://colibri.uni-graz.at/en/) and the [NeuroImaging-Lab Graz](https://neuroimaging.uni-graz.at)

<figure class="fourth">
  <img class="padding" src="{{ site.url }}{{ site.baseurl }}/images/logopic/Logo_UniGraz.png" style="height: 90px">
  <img class="padding" src="{{ site.url }}{{ site.baseurl }}/images/logopic/Logo_Colibri.jpg" style="height: 90px">
  <!-- <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/Logo_NWO.jpg" style="width: 120px">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/Logo_ERC.jpg" style="width: 110px"> -->
</figure>


# Committee

{% assign number_printed = 0 %}
{% for member in site.data.committee %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/committee_pic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i> {{ member.position }}<br>
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



