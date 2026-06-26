---
layout: page
title: Posts
permalink: /posts/
---

{% for post in site.posts %}

<article class="post-preview">

<h3>
    <a href="{{ post.url | relative_url }}">
        {{ post.title }}
    </a>
</h3>

<small class="post-meta">
    {{ post.date | date: "%d %B %Y" }}
</small>

{{ post.excerpt }}

</article>

<hr>

{% endfor %}

<hr><hr><hr>

{% for post in site.posts %}

### [{{ post.title }}]({{ post.url | relative_url }})

{{ post.date | date: "%d %B %Y" }}

{{ post.excerpt }}

---

{% endfor %}