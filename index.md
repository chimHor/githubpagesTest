---
layout: default
---
<p>site.url</p>
<p>{{ site.url }}</p>

<p>site.github.url</p>
<p>{{ site.github.url }}</p>

<p>site.baseurl</p>
<p>{{ site.baseurl }}</p>

<p> prepend</p>
<p>{{ site.url | prepend: site.baseurl}}</p>

<ul class="posts">
{% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>


