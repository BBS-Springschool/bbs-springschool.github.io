---
title: "BBS Springschool"
layout: gridlay
excerpt: "Keynotes, educationals, visits"
sitemap: false
permalink: /events/
---

<p>&nbsp;</p>

<div class="col-sm-12">
  <div class="well">
  <h2>Keynote: "Explanation and prediction of cultural change"</h2>
  <img src="{{ site.url }}{{ site.baseurl }}/images/events/igrossmann.jpeg" class="img-responsive" width="33%" style="float: right" />
  
  <ul style="list-style-type:none">
    <li><h3>Igor Grossmann Ph.D</h3></li>
    <li>Director, Wisdom and Culture Laboratory</li>
    <li>University of Waterloo, Canada</li>
    <!-- <li><a href="https://igorgrossmann.com/" target="_blank">https://igorgrossmann.com/</a></li> -->
  </ul>
<p>&nbsp;</p>
<p><strong>Date:</strong> Wednesday April 6<sup>th</sup>, 7pm (CEST)<br>
<strong>Location:</strong> <a href="https://campusplan.uni-graz.at/0002EG0048" target="_blank">HS 02.01, Universitätsplatz 2</a> and 
<strong> online </strong> via <a href="https://unitube.uni-graz.at/" target="_blank">UniTube Graz</a></p>

 <p><strong>Registration:</strong> Due to the still ongoing CoVID-pandemic <strong>registration for this event is mandatory</strong>. <a href="https://www.termino.gv.at/meet/b/54bf693805927c350a4673a3d7f42ad3-116375" target="_blank">Please register here.</a> Online participants will receive a link to the online event shortly beforehand.</p>

  <p><strong>CoVID-19 **Measures**:</strong> Access is only possible with a valid 2.5 G proof. FFP2 masks have to be worn strictly all time.</P>

<p><strong><a href="{{ site.url }}/igrossmann">Abstract and further information to this keynote.</a></strong></p>

 </div>
</div>

<p>&nbsp;</p>

# Educationals and lab-visits

We have planned educationals on a variety of topics such as science communication, design, and plain language, as well as data management, preregistration, and reproducibility. Furthermore, lab visits to the MRI-lab Graz, demos on how to collect data using NIRS, EEG, or VR. Further information will be summarized here.

{% assign number_printed = 0 %}
{% for event in site.data.events %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if event.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <eventtitle>{{ event.title }}</eventtitle>
  <p>{{ event.description }}</p>
  <p><img src="{{ site.url }}{{ site.baseurl }}/images/events/{{ event.image }}" class="img-responsive" width="25%" style="float: left" />
  <eventauthor>{{ event.authors }}</eventauthor><br>
  {{ event.about }}</p>
  <p><strong>Date:</strong> {{ event.location.time }}<br>
  <strong>Location:</strong> {{ event.location.place }}<br>
  <strong><a href="{{ event.link.url }}">{{ event.link.display }}</a></strong></p>
  
  <p class="text-danger"><strong> {{ event.alertnews }}</strong></p>
  <p> {{ event.news }}</p>
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
