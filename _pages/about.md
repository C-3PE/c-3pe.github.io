---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

## Project

The Comprehensive Personalized Programming Practice Environment (C-3PE) is an NSF-funded project aimed at enhancing introductory computer science (CS) education through the design and development of a comprehensive, personalized learning environment for programming students. This project is a collaborative effort between the University of Pittsburgh, North Carolina State University, Carnegie Mellon University, and University of Massachusetts Amherst. The C-3PE environment leverages advances in AI-driven learning technologies and, more importantly, theoretical frameworks from learning sciences to create highly engaging CS learning experiences. C-3PE will improve introductory CS education by providing ample personalized practice support and detailed feedback to students to enhance their learning experiences and outcomes. 

The growing demand for CS education, coupled with the rise of generative artificial intelligence (AI) tools in programming, stresses the importance of educational advancements in this field. These advancements must include understanding the most effective approaches to support students' learning integrated within state-of-the-art adaptive technologies that provide CS students with effective, scalable, and personalized educational support. Our project proposes and investigates novel AI-based approaches for multi-level personalization in CS education, which are capable of recommending the next learning activities most appropriate to the current level of student knowledge and supporting their work with these activities with personalized fine-grained feedback.Our research will also yield new insights in learning science. Specifically, we aim to determine the most effective practice modes (e.g., worked examples vs. practice problems) based on a student's practice history, competency levels, and current state of knowledge. The project has significant transformative potential to provide a deeper understanding of how (1) various modes of practice (2) personalization with respect to the mode of practice and individualized support can produce better learning outcomes for students. 

C-3PE will impact over 1,000 undergraduate students across a diverse range of institutions, including North Carolina State University, the University of Pittsburgh, the University of Massachusetts Amherst, and Carnegie Mellon University. The project also includes collaborations with smaller colleges, such as North Carolina A&T State University, a Historically Black College and University (HBCU). If you are interested in collaborating with the project through integrating C-3PE in your classrooms, please <a href="mailto:{{- site.data.pi | map: 'email' | join: ',' -}}" target="_blank"><i class="fa fa-envelope"></i>&nbsp;email&nbsp;us</a>.



## PIs

{% for member in site.data.pi %}

<div class="jumbotron">
<div class="row">
<div class="col-sm-2">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-9 col-xs-12">
  <h3>{{ member.name }}</h3>
  <h4><i>{{ member.title }}, {{ member.affiliation }}</i></h4>
  <p>
    {%- if member.email -%}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-3x"></i></a>{%- endif -%}
    {%- if member.cv -%}<a href="{{ site.url }}{{ site.baseurl }}/{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-3x"></i></a>{%- endif -%}
    {%- if member.scholar -%}<a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-3x"></i></a>{%- endif -%}
    {%- if member.github -%}<a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-3x"></i></a>{%- endif -%}
    {%- if member.researchgate -%}<a href="{{ member.researchgate }}" target="_blank"><i class="ai ai-researchgate-square ai-3x"></i></a>{%- endif -%}
  </p>

  <ul style="overflow: hidden">
    {% for education in member.education %}
      <li>{{ education | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>

</div>
</div>
</div>
{% endfor %}

{% if site.data.grants %}

<div class="jumbotron">
  <h3>Grants</h3>
  <ul>
    {% for grant in site.data.grants %}
      <li><a href="{{ grant.url }}">{{ grant.name }}</a></li>
    {% endfor %}
  </ul>
</div>
{% endif %}

{% if site.data.awards %}

<div class="jumbotron">
  <h3>Awards</h3>
  <ul>
    {% for award in site.data.awards %}
      <li>{{ award.name | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

{% if site.data.funders %}
<div class="jumbotron">
  <h4>Sponsors</h4>
  <div style='display:block; text-align:center; margin-left:auto; margin-right:auto;'>
  {% for funder in site.data.funders %}<a href="{{ funder.url }}" target="_blank"><img src='{{ site.url }}{{ site.baseurl }}/images/{{ funder.image }}' style='max-height: 80px; max-width: 200px; margin: 1%'/></a>{% endfor %}
  </div>
</div>
{% endif %}