---
layout: page
title: La Métaphysique 
permalink: /metaphysic/fr/
tag-name: metaphysic 
lang: fr
---

  <ul class="post-list">
	{% for post in site.posts %}
		{% if post.categories contains page.tag-name %}
			{% if post.tags contains page.lang %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <p>{{ post.excerpt }}</p>
      </li>
{% endif %} 
{% endif %} 
{% endfor %}
  </ul>
