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

{% assign team_sections = "postdoc-research::Postdoctoral Fellows & Research Scientists||students::Graduate, Medical & Undergraduate Students||visiting::Visiting Researchers" | split: "||" %}
{% for section in team_sections %}
{% assign section_parts = section | split: "::" %}
{% assign section_key = section_parts[0] %}
{% assign section_title = section_parts[1] %}
{% assign section_members = site.data.team_members | where: "group", section_key | sort: "order" %}

### {{ section_title }}

<div class="team-grid" markdown="0">
{% for member in section_members %}
<article class="team-card">
<img class="team-card__photo" src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" alt="Portrait of {{ member.name | escape }}" />
<div class="team-card__content">
<h4>{{ member.name }}</h4>
<p class="team-card__role"><i>{{ member.info }}</i></p>
{% if member.website or member.scholar or member.orcid or member.linkedin %}
<div class="team-card__links" aria-label="Profiles for {{ member.name | escape }}">
{% if member.website %}<a href="{{ member.website }}" target="_blank" rel="noopener noreferrer" aria-label="Personal website" title="Personal website"><i class="fa fa-external-link" aria-hidden="true"></i></a>{% endif %}
{% if member.scholar %}<a href="{{ member.scholar }}" target="_blank" rel="noopener noreferrer" aria-label="Google Scholar" title="Google Scholar"><i class="ai ai-google-scholar" aria-hidden="true"></i></a>{% endif %}
{% if member.orcid %}<a href="{{ member.orcid }}" target="_blank" rel="noopener noreferrer" aria-label="ORCID" title="ORCID"><i class="ai ai-orcid" aria-hidden="true"></i></a>{% endif %}
{% if member.linkedin %}<a href="{{ member.linkedin }}" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn" title="LinkedIn"><i class="fa fa-linkedin-square" aria-hidden="true"></i></a>{% endif %}
</div>
{% endif %}
<p class="team-card__bio">{{ member.bio }}</p>
</div>
</article>
{% endfor %}
</div>
{% endfor %}

## Other

<div class="team-grid" markdown="0">
{% for member in site.data.alumni %}
<article class="team-card">
<img class="team-card__photo" src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" alt="Portrait of {{ member.name | escape }}" />
<div class="team-card__content">
<h4>{{ member.name }}</h4>
<p class="team-card__role"><i>{{ member.info }}</i></p>
<p class="team-card__bio"><strong>Current:</strong> {{ member.current_degree }}</p>
</div>
</article>
{% endfor %}
</div>

## Alumni

<div class="team-grid" markdown="0">
{% for member in site.data.alumni_members %}
<article class="team-card">
<img class="team-card__photo" src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" alt="Portrait of {{ member.name | escape }}" />
<div class="team-card__content">
<h4>{{ member.name }}</h4>
<p class="team-card__role"><i>{{ member.info }}</i></p>
<p class="team-card__bio"><strong>Current:</strong> {{ member.current_degree }}</p>
{% if member.past_degree %}<p class="team-card__bio"><strong>Past:</strong> {{ member.past_degree }}</p>{% endif %}
</div>
</article>
{% endfor %}
</div>
