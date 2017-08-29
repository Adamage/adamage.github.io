---
layout: page
title: machine learning blog
tagline: Adamage Software
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## Github projects:
<a href="https://github.com/Adamage/python-training">Comprehensive, interactive Python course</a> <br>
<a href="https://github.com/Adamage/neural-nets-tutorials">Neural nets and numerical libs tutorials:</a> <br>
├── <a href="https://github.com/Adamage/neural-nets-tutorials/tree/master/tensorflow">Tensorflow</a>  <br>
└── <a href="https://github.com/Adamage/neural-nets-tutorials/tree/master/numpy-tutorials">Numpy</a> <br>
    
## Browse by tags:
<ul class="tag_box inline">
  {% assign tags_list = site.tags %}  
  {% include JB/tags_list %}
</ul>