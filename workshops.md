---
layout: posttwo 
title: Workshops
description: 'Learn how to contribute to MAgPIE'
image: assets/images/generic/lu16.jpg
style: 6
author: null
nav-menu: true
show_tile: true
collection: workshops
---



{% assign workshops = site[page.collection] | where: "landing", "true" %}

{% assign future_workshops = workshops | where:  "archived", "false" %}
{% assign past_workshops = workshops | where:  "archived", "true" %}

<p>
The following workshops are coming up in the future:




{% for t in future_workshops %}
<section>
		<a href="{{t.url}}" target = "{{ page.button_target }}" class="button">
			<img src="{{t.image}}" alt="{{ t.title }}" data-position="center center" />
		</a>
</section>
{% endfor %}
</p>

<p>
The following workshops have taken place and content contained within is archived:

</p>

{% for t in past_workshops %}
<section>
		<p>
		<a href="{{t.url}}" target = "{{ page.button_target }}" class="button">
        {{ t.title }}
		</a>
		</p>
</section>
{% endfor %}

