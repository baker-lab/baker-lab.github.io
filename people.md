---
layout: page
title: People
description: Who's in the lab
---

<section>
	<h4>Meet the team</h4>
	<p>Established in 2016, the Bakery currently consists of {{ site.categories.teamMembers | size }} members. Scroll on down to find out more about them and what they work on.</p>
	<hr />
	<img class="center" style="width: 50%;" src="{{ absolute_url }}/assets/images/Christmas_21.JPG" alt="" />
	<p class="center" style="font-weight: lighter;">The Bakery: May 2022</p>
	<hr />

	{% assign people = site.categories.teamMembers | sort: 'date'  %}
	{% for post in people %}
	{% if site.tiles-source == 'posts' %}
		<header id="{{ post.title }}">
			<h4>{{ post.title }}<span class="image right"><img src="{{ absolute_url }}/assets/images/{{ post.image }}" alt="" /></span></h4>
			{% if post.twitter %}<p><a href="https://twitter.com/{{ post.twitter }}" class="fa fa-twitter"> {{ post.twitter }}</a></p>{% endif %}
		</header>
		<h5>ROLE</h5>
		<p>{{ post.role }}</p>
		<h5>BACKSTORY</h5>
		<p>{{ post.backstory }}</p>
		<h5>RANDOM FACT</h5>
		<p>{{ post.factoid }}</p>
		<hr />
	{% endif %}
	{% endfor %}

</section>
