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
<p>{{ site.url | append: site.baseurl}}</p>

<ul class="posts">
{% for post in site.posts %}
    <p>url is </p>
    <p>{{ post.url }}</p>
    <p>{{ site.url }}</p>
    <p>{{ site.baseurl }}</p>
    <p>{{ site.baseurl | append: post.url }}</p>
    <p>{{ site.url | append: site.baseurl | append: post.url }}</p>

    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>


