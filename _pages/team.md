---
title: "Team"
layout: gridlay
sitemap: false
permalink: /team/
---

## Team

<div style="text-align: center; margin-bottom: 2rem;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/Lab_2025.JPG" alt="Lab Group Photo 2025" style="max-width: 750px; width: 100%; border-radius: 12px; box-shadow: 0 4px 16px rgba(0,0,0,0.12);" />
  <p style="color: #888; font-size: 0.9rem; margin-top: 0.5rem;">Lab retreat, 2025</p>
</div>

{% for member in site.data.team_members %}
<div class='jumbotron'>
<div class="row">
<div class="col-sm-2">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-10 col-xs-12">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br></i>

  <!-- Use the 'bio' field for team members -->
  <p><strong>Bio:</strong> {{ member.bio }}</p>
</div>
</div>
</div>
{% endfor %}

## Other

{% for member in site.data.alumni %}
<div class='jumbotron'>
<div class="row">
<div class="col-sm-2">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-10 col-xs-12">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br></i>

  <p><strong>Current:</strong> {{ member.current_degree }}</p>
</div>
</div>
</div>
{% endfor %}

## Alumni

{% for member in site.data.alumni_members %}
<div class='jumbotron'>
<div class="row">
<div class="col-sm-2">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-10 col-xs-12">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br></i>

  <p><strong>Current:</strong> {{ member.current_degree }}</p>
  {% if member.past_degree %}<p><strong>Past:</strong> {{ member.past_degree }}</p>{% endif %}
</div>
</div>
</div>
{% endfor %}

