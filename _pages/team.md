---
title: "Team"
layout: gridlay
sitemap: false
permalink: /team/
---

## Team

<div markdown="0" id="teamPhotoCarousel" class="carousel slide" data-bs-ride="carousel" data-bs-interval="5000" data-bs-pause="hover" data-bs-touch="true" style="max-width:750px; margin:0 auto 2rem;">
  <div class="carousel-indicators">
    <button type="button" data-bs-target="#teamPhotoCarousel" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Lab photo 1"></button>
    <button type="button" data-bs-target="#teamPhotoCarousel" data-bs-slide-to="1" aria-label="Lab photo 2"></button>
    <button type="button" data-bs-target="#teamPhotoCarousel" data-bs-slide-to="2" aria-label="Lab photo 3"></button>
    <button type="button" data-bs-target="#teamPhotoCarousel" data-bs-slide-to="3" aria-label="Lab photo 4"></button>
  </div>
  <div class="carousel-inner" style="border-radius:12px; box-shadow:0 4px 16px rgba(0,0,0,0.12); overflow:hidden;">
    <div class="carousel-item active">
      <img src="{{ site.url }}{{ site.baseurl }}/images/Lab_2025.JPG" class="d-block w-100" alt="Lab members at the 2025 retreat" style="width:100%; aspect-ratio:4 / 3; object-fit:cover; margin:0; border-radius:0;" />
      <div class="carousel-caption" style="left:50%; right:auto; bottom:1rem; transform:translateX(-50%); width:max-content; max-width:calc(100% - 4rem); padding:0.35rem 0.8rem; background:rgba(0,0,0,0.58); border-radius:6px;">
        <p style="margin:0; color:#fff; font-size:0.9rem;">Lab retreat, 2025</p>
      </div>
    </div>
    <div class="carousel-item">
      <img src="{{ site.url }}{{ site.baseurl }}/images/Lab_2026.jpg" class="d-block w-100" alt="Lab members viewing media coverage of the Kamineni et al. study in 2026" style="width:100%; aspect-ratio:4 / 3; object-fit:cover; margin:0; border-radius:0;" />
      <div class="carousel-caption" style="left:50%; right:auto; bottom:1rem; transform:translateX(-50%); width:max-content; max-width:calc(100% - 4rem); padding:0.35rem 0.8rem; background:rgba(0,0,0,0.58); border-radius:6px;">
        <p style="margin:0; color:#fff; font-size:0.9rem;">Kamineni et al. featured by HMS and MGB, 2026 (1)</p>
      </div>
    </div>
    <div class="carousel-item">
      <img src="{{ site.url }}{{ site.baseurl }}/images/Lab_2026_2.jpg" class="d-block w-100" alt="Lab members viewing media coverage of the Kamineni et al. study in 2026, second photo" style="width:100%; aspect-ratio:4 / 3; object-fit:cover; margin:0; border-radius:0;" />
      <div class="carousel-caption" style="left:50%; right:auto; bottom:1rem; transform:translateX(-50%); width:max-content; max-width:calc(100% - 4rem); padding:0.35rem 0.8rem; background:rgba(0,0,0,0.58); border-radius:6px;">
        <p style="margin:0; color:#fff; font-size:0.9rem;">Kamineni et al. featured by HMS and MGB, 2026 (2)</p>
      </div>
    </div>
    <div class="carousel-item">
      <img src="{{ site.url }}{{ site.baseurl }}/images/Celebration_2026.jpg" class="d-block w-100" alt="Lab members celebrating students in 2026" style="width:100%; aspect-ratio:4 / 3; object-fit:cover; margin:0; border-radius:0;" />
      <div class="carousel-caption" style="left:50%; right:auto; bottom:1rem; transform:translateX(-50%); width:max-content; max-width:calc(100% - 4rem); padding:0.35rem 0.8rem; background:rgba(0,0,0,0.58); border-radius:6px;">
        <p style="margin:0; color:#fff; font-size:0.9rem;">Celebration for students, 2026</p>
      </div>
    </div>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#teamPhotoCarousel" data-bs-slide="prev" aria-label="Previous lab photo">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#teamPhotoCarousel" data-bs-slide="next" aria-label="Next lab photo">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
  </button>
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
