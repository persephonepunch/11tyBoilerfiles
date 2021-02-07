---
title: Welcome
date: Created
layout: page
tags:
  - home
  - welcome
  - info
---
<div class="wrapper">
<div class="uk-child-width-1-1 uk-child-width-1-3@s uk-margin" uk-grid>
  {%- for item in collections.post | reverse | limit(9) -%}
    <div class="uk-card uk-card-body uk-card-default uk-card-hover">
                <h4 class="uk-card-title">{{item.data.title}}</h4>
                <p >{{item.data.summary}}</p>
                <button class="uk-button uk-button-primary uk-light"><a href="{{ item.url | url }}">Read More</a></button>
    </div>
  {%- endfor -%}
 
</div>
</div>
 
 