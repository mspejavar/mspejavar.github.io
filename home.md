---
layout: page
title: Home
permalink: /home/
published: true
order: 1
---

<div class="media">
	<div class="media-img"><img src="http://52.76.68.253/blog/img/index-recent.jpg" alt=""></div>
	<div class="media-bd text-center">
	<p class="intro">Hello Everyone! I am Dhatri Rao and I welcome you all to my space where I’d love to take you all through the various tastes of my endless Fashion Journey.</p>
	<ul class="list">
		<li><a target="_blank" href="{{ site.instagram}}"><i class="fa fa-2x fa-instagram"></i></a></li>
		<li><a target="_blank" href="{{ site.facebook}}"><i class="fa fa-2x fa-facebook"></i></a></li>
		<li><a target="_blank" href="{{ site.wooplr}}"><img src="https://www.wooplr.com/images/jiggle-icon-1439884301966.png" alt="wooplr" height="28"></a></li>
	</ul>
	</div>
</div>

{% include blog.html %}

{% for page in site.pages %}
{% if page.name == 'about.md' %}
<div class="section">
        <h1 class='section-head'>About Me </h1>
<div id="about" class="post">
{{ page.content | truncatewords: 100 }}
<p><a href="{{ page.url }}" class="btn">Read More&hellip;</a></p>
</div>
    </div>
{% endif %}
{% endfor %}