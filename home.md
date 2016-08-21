---
layout: page
title: Home
permalink: /home/
published: true
order: 1
---

<div class="post">
<img src="http://52.76.68.253/blog/img/index-recent.jpg" alt="">
<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo, quae tempora sed exercitationem autem est debitis, illo error repudiandae voluptates soluta, voluptatum beatae, similique aliquam temporibus doloremque. Reprehenderit rem, non.</p>
</div>
<h1 class='section-head'>Blogs</h1>
{% include blog.html %}

{% for page in site.pages %}
{% if page.name == 'about.md' %}
<div class="section">
        <h1 class='section-head'>About Me </h1>
<div id="about" class="post">
{{ page.content | truncatewords: 100 }}
<p><a href="{{ page.url }}" class="btn">Read More</a></p>
</div>
{% endif %}
{% endfor %}