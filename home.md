---
layout: page
title: Home
permalink: /home/
published: true
order: 1
---

<div class="media">
	<div class="media-img"><img src="http://52.76.68.253/blog/img/index-recent.jpg" alt=""></div>
        <div class="media-img" style="padding-left:10px"><img src="/images/upcoming.jpg" alt="" style="width:100%; height:400px;"></div>
</div>
<h1 class='section-head'>Blogs</h1>
{% include blog.html %}

{% for page in site.pages %}
{% if page.name == 'about.md' %}
<div class="section">
        <h1 class='section-head'>About Me </h1>
<div id="about" class="post">
<p style="font-weight:bold;font-size:x-large;">Unleashing a New Life</p>
{{ page.content | truncatewords: 35 }}
<p><a href="{{ page.url }}" class="btn">Read More&hellip;</a></p>
</div>
    </div>
{% endif %}
{% endfor %}