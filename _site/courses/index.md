---
title: Courses
layout: page
eleventyNavigation:
  key: courses
  parent: main
---
 
# {{title}}

<div class="wrapper">
<div class="uk-child-width-1-1 uk-child-width-1-3@s uk-margin" uk-grid>
  {%- for course in courses | reverse | limit(9) -%}
     <div class="uk-card" >
      <img data-src="{{ course.thumbnail | safe }}" alt="{{ course.title | safe }}" uk-img>
      <div class="uk-card-body">
        <h5>{{ course.title | safe }}</h5>
        <time class="item-date small d-block text-muted mb-2"
          datetime="{{ course.date | safe }}">{{ course.date | courseDate }}</time>
        <p >{{ course.summary | safe }}</p>
        <a href="{{ course.url | url }}"  target="_blank">Watch course</a>
      </div>
    </div>
  {% endfor %}
</div>
</div>








