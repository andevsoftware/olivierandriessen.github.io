---
layout: page
title: Archive
---

{% for post in site.posts %}

<h1 class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></h1>
<div class="post-date">
{{ post.date | date_to_string }}
</div>
{{ post.excerpt }}

{% endfor %}