---
layout: default
permalink: /cv
---
<section class="cv container">
  {%- include cv/header.liquid -%}

  {%- if jekyll.environment == 'production' and site.gtm -%}
  {%- include gtm_body.html -%}
  {%- endif -%}

  {%- include cv/about.liquid content=site.data.cv.about_me -%}

  {% if site.data.cv.skills %}
    <div class="list-container">
      <h3 id="скиллы">Скиллы</h3>
      {% include cv/skills.liquid content=site.data.cv.skills %}
    </div>
  {% endif %}

  {% if site.data.cv.experience %}
    <div class="list-container">
      <h3 id="опыт-работы">Опыт работы ({{ site.data.cv.experience.total }})</h3>
      {% include cv/experience.liquid content=site.data.cv.experience %}
    </div>
  {% endif %}

  {% if site.data.cv.articles %}
    <div class="list-container">
      <h3 id="статьи">Статьи</h3>
      {% include cv/articles.liquid content=site.data.cv.articles %}
    </div>
  {% endif %}


  {% if site.data.cv.projects %}
    <div class="list-container">
      <h3 id="проекты">Проекты</h3>
      {% include cv/projects.liquid content=site.data.cv.projects %}
    </div>
  {% endif %}

  {% if site.data.cv.education %}
    <div class="list-container">
      <h3 id="образование">Образование</h3>
      {% include cv/education.liquid content=site.data.cv.education %}
    </div>
  {% endif %}
</section>