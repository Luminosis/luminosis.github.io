---
layout: page
title: La Vérité
permalink: /truth/fr/
tag-name: truth
lang: fr
---

  <!-- h1 class="page-heading">VERITE</h1 -->

	
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
  
<p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>
