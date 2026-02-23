---
title: "Team"
layout: gridlay
sitemap: false
permalink: /team/
---

## Principal Investigators

{% for member in site.data.pi %}
<div class="pi-card" markdown="0">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" alt="{{ member.name }}"/>
<div class="pi-info">
<h4>{{ member.name }}</h4>
<div class="pi-title">{{ member.title }}, {{ member.affiliation }}</div>
<div class="pi-links">
{% if member.website %}<a href="{{ member.website }}" target="_blank"><i class="fa fa-home fa-lg"></i></a>{% endif %}
{% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-lg"></i></a>{% endif %}
{% if member.scholar %}<a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-lg"></i></a>{% endif %}
{% if member.github %}<a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-lg"></i></a>{% endif %}
{% if member.researchgate %}<a href="{{ member.researchgate }}" target="_blank"><i class="ai ai-researchgate-square ai-lg"></i></a>{% endif %}
{% if member.orcid %}<a href="https://orcid.org/{{ member.orcid }}"><i class="ai ai-orcid-square ai-lg"></i></a>{% endif %}
</div>
</div>
</div>
{% endfor %}

## Current Students

<div class="student-grid" markdown="0">
{% for member in site.data.team_members %}
<div class="student-card">
{% if member.photo %}
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" alt="{{ member.name }}"/>
{% else %}
<div class="student-placeholder">{{ member.name | slice: 0 }}</div>
{% endif %}
<h5>{{ member.name }}</h5>
<div class="student-title">{{ member.title }}</div>
<div class="student-links">
{% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square"></i></a>{% endif %}
{% if member.website %}<a href="{{ member.website }}" target="_blank"><i class="fa fa-home"></i></a>{% endif %}
{% if member.scholar %}<a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square"></i></a>{% endif %}
{% if member.github %}<a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square"></i></a>{% endif %}
</div>
</div>
{% endfor %}
</div>

{% if site.data.alumni %}
## Former Contributors

<ul class="alumni-list">
{% for member in site.data.alumni %}
  <li><strong>{{ member.name }}</strong> &mdash; {{ member.info }}{% if member.duration %} ({{ member.duration }}){% endif %}</li>
{% endfor %}
</ul>
{% endif %}

<div class="opportunities-section">

### Opportunities to Join

If you are interested in joining this project, please apply to one of the PhD programs listed below and mention the project member you would like to work with:

- [Intelligent Systems PhD Program (UPitt)](https://www.sci.pitt.edu/academics/doctoral-degrees/intelligent-systems-phd)
- [Information Science PhD Program (UPitt)](https://www.sci.pitt.edu/academics/doctoral-degrees/information-science-phd)

</div>
