---
layout: page
pagination:
  data: collections.post
  size: 5
eleventyExcludeFromCollections: true
permalink: /posts/{{pagination.pageNumber}}/
---

<h1>Posts</h1>

{% include "pagination.njk" %}
{%- for item in pagination.items -%}
  <div class="uk-grid">
    <div class="uk-panel">
      <div>
        <img data-src="{{item.data.thumbnail}}" alt="{{item.title}}" uk-image>
        <time datetime="{{item.date }}">{{item.date | simpleDate}}</time>
      </div>
      <div>
        <h4>{{item.data.title}}</h4>
        <p >{{item.data.summary}}</p>
      </div>
    </div>
  <div class="uk-light">
    <a class="uk-button uk-button-primary" href="{{ item.url | url }}" >read more</a>
  </div>
</div>
{%- endfor -%}
{% include "pagination.njk" %}
