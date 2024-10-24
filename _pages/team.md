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
  {%- include socials.html -%}
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
{% if site.data.team.visitor.size > 0 %}
## Visiting Researchers
{% endif %}

{% assign number_printed = 0 %}
{% for member in site.data.team.visitor %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <!-- Member photo floats on left -->
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  
  <h4>{{ member.name }}</h4>
  {%- include socials.html -%}
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
{% if site.data.team.currentstudents.size > 0 %}
## Current Students
{% endif %}

{% assign number_printed = 0 %}
{% for member in site.data.team.currentstudents %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <!-- Member photo floats on left -->
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  
  <h4>{{ member.name }}</h4>
  {%- include socials.html -%}
  <i>{{ member.info }}</i>
  
  <!--{% if member.advisor.size == 1 %}
  Advisor: <i>{{ member.advisor }}</i>
  {% endif %}
  {% if member.advisor.size > 1 %}
  Advisors: <i>{{ member.advisor[0] }}</i>, <i>{{ member.advisor[1] }}</i>
  {% endif %} -->
 
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


## Interested in Joining the Lab?
We are a new lab on the lookout for talented and driven graduate students to engage in exciting, meaningful, 
and challenging research in ocean optics and particle dynamics.

#### Postdoctoral Researchers
We are currently looking for a postdoctoral researcher to join the Slade Lab in 2025. \[coming soon\]

#### Graduate Students
<!-- More details here -->
There are no research assistantship opportunities currently available in the Slade Lab.

For more information on the graduate programs at FAU HBOI including admission requirements and other funding opportunities see the Graduate College's 
[Ph.D. Integrative Biology](https://www.fau.edu/hboi/education-and-outreach/graduate-programs/phd-integrative-biology/) and
[M.S. Marine Science & Oceanography (MSO)](https://www.fau.edu/hboi/education-and-outreach/graduate-programs/ms-marine-science-and-oceanography/) programs.
Many of our lab interests and ongoing projects include numerical modeling and instrument development that may overlap with other graduate programs like 
Electrical Engineering. Get in touch if you're an engineer with a passion for working on developing ocean optical instrumentation and methods.
 

#### Undergraduates
If you are an FAU undergraduate looking for a possible capstone or honors project, please contact us.




<!----------------------------------------------------------------------------------------------------------------------------------------->
{% if site.data.team.alumni.size > 0 %}
## Lab Alumni
{% endif %}

<div class="row">
{% for member in site.data.alumni %}
<div class="col-sm-6 clearfix">
  <h4>{{ member.name }}</h4>
  <i> {{ member.role }}</i>
</div>
{% endfor %}
</div>
