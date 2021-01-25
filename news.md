---
layout: page
title: News
description: Some of our latest stories
---

<section>
	<h4>Lab News</h4>
	<p>Catch up on some of our latest stories.</p>
	<hr />

	{% assign news = site.categories.news | sort: 'date' | reverse  %}
	{% for post in news %}
	{% if site.tiles-source == 'posts' %}
		<header id="{{ post.title }}">
			<h4>{{ post.title }}<span class="image right"><img src="{{ absolute_url }}/assets/images/{{ post.image }}" alt="" /></span></h4>
            <p>{{ post.date | date: "%b %d, %Y" }}</p>
			{% if post.twitter %}<p><a href="https://twitter.com/{{ post.twitter }}" class="fa fa-twitter"> {{ post.twitter }}</a></p>{% endif %}
		</header>
        {{ post.content }}
		<hr />
	{% endif %}
	{% endfor %}

</section>
