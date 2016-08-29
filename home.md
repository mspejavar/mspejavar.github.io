---
layout: page
title: Home
permalink: /home/
published: true
order: 1
---

<div class="media">
	<div class="media-img"><img src="/images/index-recent.jpg" alt=""></div>
	<div class="media-bd" style="padding-left:28px;">
                <a href="/street/2016/08/29/the-skirt-affair.html">
		<div style="background:url('/images/upcoming.jpg') no-repeat;height:400px;padding: 10px 24px;">
			<p style="background-color: rgba(0,0,0,0.8);padding: 10px;font-size: 24px; font-family:Cormorant;margin-top: 300px;">Upcoming Post: Street Girl feat. Skirt</p>
		</div></a>
	</div>
</div>

<div class="section">
	<h1 class='title'>Blogs </h1>
	{% include blog.html %}
</div>

{% for page in site.pages %}
{% if page.name == 'about.md' %}
<div class="section">
        <h1 class='section-head'>About Me </h1>
<div id="about" class="post">
    <p style="font-weight:bold;font-size:x-large;">Unleashing a New Life...</p>
{{ page.content | truncatewords: 35 }}
<p><a href="{{ page.url }}" class="btn">Read More&hellip;</a></p>
</div>
{% endif %}
{% endfor %}
