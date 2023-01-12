---
layout: page
permalink: /people/
title: People
nav: true
nav_order: 1
---

{% for person in site.data.members %}
<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div id = "{{person.name}}" class="row" style="padding-top: 60px; margin-top: -60px;">
    {% if person.image %}<img style="float: right; width: 42%; padding-left: 20px;" src="{{ person.image | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}" alt="photo of {{person.name}}">{% endif %}
    <div>
        <h4>{{person.name}}{% if person.degrees %}, {{person.degrees}} {% endif %}</h4> 
        {{person.position}} <br>
        <i class="fa fa-envelope"></i> <a href= "{{mailto:person.email}}" target="_blank">{{person.email}}</a> <br>
        {% if person.website %}
          <i class="fa fa-globe"></i> <a href= "{{person.website}}" target="_blank">{{person.website}}</a> <br>
        {% endif %}
        {% if person.github %}
          <i class="fab fa-github"></i> <a href= "https://github.com/{{person.github}}" target="_blank"> {{person.github}} </a> <br>
        {% endif %}
        {% if person.scholar %}
          <i class="ai ai-google-scholar"></i> <a href= "http://scholar.google.com/citations?user={{person.scholar}}" target="_blank"> Scholar </a> <br>
        {% endif %}
        {% if person.orcid %}
          <i class="ai ai-orcid"></i> <a href="http://{{person.orcid}}" target="_blank"> {{person.orcid}}</a> <br>
        {% endif %}
    </div>
    <div class="col-sm-8">
        <p>{{person.description | markdownify}}</p>
    </div>
</div>
<hr>
{% endfor %}

---

## Past members
{% for alum in site.data.alumni %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div id = "{{alum.name}}" class="row" style="padding-top: 60px; margin-top: -60px; padding-bottom: 20px;">
  <div>
    <strong>{{alum.name}}{% if alum.degrees %}, {{alum.degrees}} {% endif %}</strong> <br>
    <i>previously:</i> {{alum.previously}} <br>
    <i>now:</i> {{alum.now}}<br>
      {% if alum.website %} <i class="fa fa-globe"></i> <a href= "{{alum.website}}" target="_blank">{{alum.website}}</a>  {% endif %}
    <i class="fa fa-envelope"></i> <a href= "{{mailto:person.email}}" target="_blank">{{person.email}}</a> <br>
  </div>
</div>
{% endfor %}
