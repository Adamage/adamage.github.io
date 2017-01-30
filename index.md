---
layout: page
title: Neural Nets tutorials & news
tagline: NLP, business data, audio, images
---
{% include JB/setup %}

## Browse by tags:

{% assign tags = "" %}
{% for tag in rawtags %}
	{% if tag != "" %}
		{% if tags == "" %}
			{% assign tags = tag | split:'|' %}
		{% endif %}
		{% unless tags contains tag %}
			{% assign tags = tags | join:'|' | append:'|' | append:tag | split:'|' %}
		{% endunless %}
	{% endif %}
{% endfor %}

{% for tag in tags %}
	<a href="#{{ tag | slugify }}"> {{ tag }} </a>
{% endfor %}

## Posts:

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## Training materials:
`http://cs224d.stanford.edu/syllabus.html`<br>
`http://www.deeplearningweekly.com/pages/open_source_deep_learning_curriculum`<br>
`https://deeplearningstudies.slack.com/messages/general/`<br>