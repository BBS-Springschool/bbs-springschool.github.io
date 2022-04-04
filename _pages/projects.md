---
title: "BBS Springschool"
layout: gridlay
excerpt: "Projects"
sitemap: false
permalink: /projects/
---


# Project submission

You have a good idea and want to work on it ,possibly, together with others? Submit! Project submission for the BBS Springschool 2022 will open on the 1<sup>st</sup> of March. Do not hesitate to [contact us]({{ site.url }}/contact) if you are not sure about your project's fit, or don’t know how to fill in the submission form.

<center style="padding-top: 3em; padding-bottom: 3em;"><a  href="https://forms.gle/NHVhCj1MxFMgr9xi9" target="_blank"><button class="fs-1 btn btn-secondary btn-lg " type="submit" value="Send"><div class="h1">Submit a project</div></button></a></center>


Following project submission, check out the advices and suggestions curated from the many previous years’ project leaders and attendees as the best practices of running successful, collaborative projects that would lead high impact and successful outputs in the given short amount of time.


## Submitted projects  (more to come)

{% assign number_printed = 0 %}
{% for project in site.data.projectlist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if project.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix">
 <div class="well">
  <pubtit>{{ project.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/project_pic/{{ project.image }}" class="img-responsive" width="12%" style="float: left" />
  <p>{{ project.description }}</p>
  <p><em>{{ project.authors.name }} ({{ project.authors.mail }})</em></p>
  <p class="text-danger"><strong> {{ project.news1 }}</strong></p>
  <p> {{ project.news2 }}</p>
  <p>
  <!-- <center> -->
  <strong> Location: {% if project.link.location %}{{ project.link.location }}{% endif %}  via {% if project.link.url %}<a href="{{ project.link.url }}">Project site</a>{% endif %}{% if project.link.url and project.link.github %} | {% endif %}{% if project.link.github %}<a href="{{ project.link.github }}">Github site</a>{% endif %}{% if project.link.url and project.link.mattermost %} | {% endif %}{% if project.link.mattermost %} <a href="{{ project.link.mattermost }}">Mattermost</a>{% endif %}{% if project.link.channel and project.link.mattermost %} | {% endif %}{% if project.link.channel %} <a href="{{ project.link.channel-link }}">{{ project.link.channel }}</a>{% endif %}
  </strong>
  <!-- </center> -->
  </p>
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
{% endif %} -->
