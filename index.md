---
layout: page
title: Neural Nets tutorials
tagline: NLP, business data, audio, images
---
{% include JB/setup %}

## Browse by tags:
<ul class="tag_box inline">
  {% assign tags_list = site.tags %}  
  {% include JB/tags_list %}
</ul>

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