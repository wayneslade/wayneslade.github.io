---
title: "Slade Lab @ FAU HBOI - People"
layout: gridlay
excerpt: "Slade Lab at Florida Atlantic University Harbor Branch: People"
sitemap: false
permalink: /team/
---

<!-- # Group Members -->
<!-- **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!** -->

<!-- Jump to [staff](#staff), [master and bachelor students](#master-and-bachelor-students), [alumni](#alumni), [administrative support](#administrative-support), [lab visitors](#lab-visitors). -->

<!-- see https://github.com/USC-NSL/USC-NSL.github.io --!>

<!----------------------------------------------------------------------------------------------------------------------------------------->
## Faculty and Staff

{% assign number_printed = 0 %}
{% for member in site.data.team.facultystaff %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <!-- Member photo floats on left -->
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
{% if member.social.website %}<a target="blank" href="{{member.social.website}}"><i class="fas fa-globe fa-lg"></i></a>{% endif %} {% if member.social.google-scholar %}<a target="blank" href="{{member.social.googlescholar}}"><i class="fab fa-google-scholar fa-lg"></i></a>{% endif %} {% if member.social.linkedin %}<a target="blank" href="{{member.social.linkedin}}"><i class="fab fa-linkedin fa-lg"></i></a>{% endif %} {% if member.social.github %}<a target="blank" href="{{member.social.github}}"><i class="fab fa-github fa-lg"></i></a>{% endif %} {% if member.social.twitter %}<a target="blank" href="{{member.social.twitter}}"><i class="fab fa-x-twitter fa-lg"></i></a>{% endif %} {% if member.social.orcid %}<a target="blank" href="{{member.social.orcid}}"><i class="fab fa-orcid fa-lg"></i></a>{% endif %} {% if member.social.research-gate %}<a target="blank" href="{{member.social.researchgate}}"><i class="ai ai-researchgate-square ai-lg"></i></a>{% endif %}  
  
  <i>{{ member.info }}</i>
  <!-- Maybe add education/notes here... -->
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


<!----------------------------------------------------------------------------------------------------------------------------------------->
## Current Students

{% assign number_printed = 0 %}
{% assign stud_array = site.data.team.currentstudents %}
<!-- Inspect a variable in liquid -->
<!-- {{ stud_array[0] | inspect }} -->

{% for member in stud_array%}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">

  {% if member.social.website %}

  {% if member.photo %}
  <a target="blank" href="{{ member.social.website }}"><img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" /></a>
  {% endif %}
  <h4><a target="blank" href="{{ member.social.website }}">{{ member.name }}</a></h4>
  {% else %}

  {% if member.photo %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  {% endif %}
  <h4>{{ member.name }}</h4>
  
  {% endif %}
  
  {%- include socialmedia.html -%}
  <i>{{ member.info }}</i><!--<br>email: <{{ member.email }}></i> -->
  {% if member.advisor.size == 1 %}
  Advisor: <i>{{ member.advisor }}</i>
  {% endif %}

  {% if member.advisor.size > 1 %} <!-- Generally a student is advised by max of 2 professors -->
  Advisor: <i>{{ member.advisor[0] }}</i>, <i>{{ member.advisor[1] }}</i>
  {% endif %}
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


<!----------------------------------------------------------------------------------------------------------------------------------------->
{% if site.data.team.visitor.size > 0 %}
## Visitor
{% endif %}

{% assign number_printed = 0 %}
{% for member in site.data.team.visitor%}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">

  {% if member.social.website %}

  {% if member.photo %}
  <a target="blank" href="{{ member.social.website }}"><img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" /></a>
  {% endif %}
  <h4><a target="blank" href="{{ member.social.website }}">{{ member.name }}</a></h4>
  {% else %}

  {% if member.photo %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  {% endif %}
  <h4>{{ member.name }}</h4>

  {% endif %}

  {%- include socialmedia.html -%}
  <i>{{ member.info }}</i> <!--<br>email: <{{ member.email }}></i> -->

  {% if member.from %}
  <i>{{ member.from }}</i>
  {% endif %}
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




<!----------------------------------------------------------------------------------------------------------------------------------------->
## Alumni
<div class="row">
{% for member in site.data.alumni %}
<div class="col-sm-6 clearfix">
  <h4>{{ member.name }}</h4>
  <i> {{ member.role }}</i>
</div>
{% endfor %}
</div>
