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

Globe <i class="fas fa-globe fa"></i> <br>
Envelope <i class="fas fa-envelope-open"></i> <br>
GoogleScholar <i class="ai ai-google-scholar-square ai-1x"></i> <br>
GitHub <i class="fab fa-github"></i> <br>
LinkedIn <i class="fab fa-linkedin"></i> <br>
Twitter <i class="fab fa-twitter"></i> <br>
ORCiD <i class="fab fa-orcid"></i> <br>
ResearchGate <i class="fab fa-researchgate"></i> <br>
<br> 
<br>

Globe <i class="fas fa-globe fa-xl"></i> 
Envelope <i class="fas fa-envelope-open fa-xl"></i> 
GoogleScholar <i class="ai ai-google-scholar-square ai-1x"></i> 
GitHub <i class="fab fa-github fa-xl"></i> 
LinkedIn <i class="fab fa-linkedin fa-xl"></i>
Twitter <i class="fab fa-twitter fa-xl"></i> 
ORCiD <i class="fab fa-orcid fa-xl"></i> 
ResearchGate <i class="fab fa-researchgate fa-xl"></i> 

<!----------------------------------------------------------------------------------------------------------------------------------------->
## Faculty and Staff

{% assign number_printed = 0 %}
{% assign fac_array = site.data.team.facultystaff | sort: "lastname" %}
{% for member in fac_array %}

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
{% assign stud_array = site.data.team.current-students | sort: "lastname" %}
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
