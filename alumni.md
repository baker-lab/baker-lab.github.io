---
layout: page
title: Alumni
description: Who's come through the lab?
---

<section>
	<h4>Our Alumni</h4>
	<p>We are happy to have hosted wonderful PhD students, PDRAs and, visitors in the Bakery. Scroll on down to find out more about our past members, their experiences with the Bakery and their next steps.</p>
	<hr />
	<img class="center" style="width: 50%;" src="{{ absolute_url }}/assets/images/alumni.jpg" alt="" />
	<hr />

	{% assign people = site.categories.alumni | sort: 'date'  %}
	{% for post in people %}
	{% if site.tiles-source == 'posts' %}
		<header id="{{ post.title }}">
			<h4>{{ post.title }}<span class="image right"><img src="{{ absolute_url }}/assets/images/{{ post.image }}" alt="" /></span></h4>
			{% if post.twitter %}<p><a href="https://twitter.com/{{ post.twitter }}" class="fa fa-twitter"> {{ post.twitter }}</a></p>{% endif %}
		</header>
		<h5>BACKSTORY</h5>
		<p>{{ post.backstory }}</p>
		<h5>EXPERIENCE IN THE BAKERY</h5>
		<p>{{ post.experience }}</p>
		<h5>NEXT STEPS</h5>
		<p>{{ post.nextsteps }}</p>
		<hr />
	{% endif %}
	{% endfor %}

</section>
