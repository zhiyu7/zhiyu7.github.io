---
title: "Media"
layout: gridlay
sitemap: false
permalink: /media/
---

## Media

<p class="media-intro">Selected coverage of our research.</p>

<div markdown="0" class="media-list">
{% for feature in site.data.media %}
  <article class="media-feature">
    <a class="media-feature__image-link" href="{{ feature.primary_url }}" target="_blank" rel="noopener noreferrer" aria-label="Read {{ feature.title }}">
      <img class="media-feature__image" src="{{ site.url }}{{ site.baseurl }}/images/{{ feature.image }}" alt="{{ feature.image_alt }}" />
    </a>
    <div class="media-feature__content">
      <p class="media-feature__eyebrow">Media coverage</p>
      <h3 class="media-feature__title"><a href="{{ feature.primary_url }}" target="_blank" rel="noopener noreferrer">{{ feature.title }}</a></h3>
      <p class="media-feature__outlet">{{ feature.outlet }}</p>
      <p class="media-feature__date">{{ feature.date }}</p>
      <p class="media-feature__tag">{{ feature.tag }}</p>
      <div class="media-feature__links" aria-label="Coverage links">
      {% for link in feature.links %}
        <a href="{{ link.url }}" target="_blank" rel="noopener noreferrer">{{ link.label }}</a>
      {% endfor %}
      </div>
    </div>
  </article>
{% endfor %}
</div>
