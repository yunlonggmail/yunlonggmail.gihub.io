---
layout: page
title: Archive
description: ''
header-img: img/orange.jpg
---

{% for post in site.posts %} {% capture y %}{{post.date | date:"%Y"}}{% endcapture %} {% if year != y %} {% assign year = y %} - {{ y }} {% endif %} -

<time datetime="{{ post.date | date:" %y-%m-%d"="" }}"="">{{ post.date | date:"%Y-%m-%d" }}</time>

[{{ post.title }}]({{ post.url }} "{{ post.title }}") {% endfor %}
