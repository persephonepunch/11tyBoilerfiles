---
pagination:
  data: clients
  size: 1
  alias: client
permalink: 'clients/{{client.name | slug }}/'
layout: page
---

<h1>{{client.name}}</h1>
<p>{{client.title}}, <span>{{client.company}}</span></p>

<img data-src="{{client.profile_photo}}" uk-image alt="{{client.name}}" uk-img>

<h2>Friends</h2>

<p > 
{% for friend in client.friends %}
{% pairedClient friend.name %}
<span uk-icon="heart"></span>
{% endpairedClient %}
{% endfor %}
</p>

<h2 >Posts</h2>

{% for post in client.posts %}

---

#### {{post.title}}

<time 
  datetime="{{ course.date | safe }}">{{ post.date_created | safe }}</time>

<p>{{post.text}}</p>

{% endfor %}
