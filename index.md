---
layout: default
title: Home
---

# Welcome

New website!

---

## Recent Posts

<ul class="posts-list">
{% for post in site.posts limit:5 %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <div class="post-date">{{ post.date | date: "%B %-d, %Y" }}</div>
    {% if post.excerpt %}
    <div class="post-excerpt">{{ post.excerpt | strip_html | truncate: 120 }}</div>
    {% endif %}
  </li>
{% endfor %}
{% if site.posts.size == 0 %}
  <li style="color:#888; font-size:11px;">No posts yet.</li>
{% endif %}
</ul>

{% if site.posts.size > 5 %}
<p style="margin-top:12px;"><a href="{{ '/posts' | relative_url }}" style="font-size:11px;">View all posts -></a></p>
{% endif %}
