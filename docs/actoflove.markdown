---
layout: page
title: L'Acte d'Amour 
permalink: /actoflove/fr/
tag-name: actoflove
lang: fr
---

  <ul class="post-list">
	{% for post in site.posts %}
		{% if post.categories contains page.tag-name %}
			{% if post.tags contains page.lang %}
      <li>
        <span class="post-meta">{{ post.date | date: " %Y, %b %-d" }}</span>
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <p>{{ post.excerpt }}</p>
      </li>
{% endif %} 
{% endif %} 
{% endfor %}
  </ul>
  
<p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

