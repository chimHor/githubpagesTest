## 个人技术笔记

<ul class="posts">
{% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url | prepend: site.github.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>


