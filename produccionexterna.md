---
layout: default
---

{% assign items = site.data.programas_externos %}

<div class="enlaces-audio">

  <!-- ========================= -->
  <!-- PODCASTS -->
  <!-- ========================= -->

  <h1>Podcasts Independientes</h1>

  <div class="grid-links">
    {% for item in items %}
      {% if item.tipo == "podcast" %}
        <a href="{{ item.url }}" target="_blank" class="grid-link">
          {{ item.nombre }}
        </a>
      {% endif %}
    {% endfor %}
  </div>

  <!-- ========================= -->
  <!-- OTRAS RADIOS -->
  <!-- ========================= -->

  <h1>Programas pinchados de otras radios libres</h1>

  <div class="radios-grid">

  {% for item in items %}
    {% if item.tipo == "radio" %}

      <div class="radio-card">

        <h3 class="radio-titulo">
          <a href="{{ item.radio.url }}" target="_blank">
            {{ item.radio.nombre }}
          </a>
        </h3>

        <div class="radio-programas">
          {% for programa in item.programas %}
            <a href="{{ programa.url }}" target="_blank" class="radio-programa">
              {{ programa.nombre }}
            </a>
          {% endfor %}
        </div>

      </div>

    {% endif %}
  {% endfor %}

</div>
</div>
