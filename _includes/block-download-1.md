{% if section.media_alignment and section.media_alignment == "Left" %}
{% include block-feature-2.html %}
{% else %}
<section class="block block-feature-1">
  <div class="container">
    <div class="columns">
      <div class="column text">
        <h2><span class="light">{{ section.headline }}</span></h2>
        <p>{{ section.content }}</p>
        {% if section.cta and section.cta.enabled == true %}
        <a class="button primary inverted" href="{{ section.cta.url }}">{{ section.cta.button_text }}</a>
        <div class="morelinks">
            <a href="https://github.com/bottlesdevs/Bottles#build-with-meson-construction_worker">Source code</a> | <a href="https://github.com/bottlesdevs/Bottles#unofficial-packages">Unofficial packages</a>
        </div>
        {% endif %}
      </div>
      <div class="column media">
        <img src="{{ section.media.image | relative_url }}" alt="{{ section.media.alt_text }}" loading="lazy">
      </div>
    </div>
  </div>
</section>
{% endif %}