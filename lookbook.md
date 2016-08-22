---
layout: page
title: Lookbook
permalink: /lookbook/
published: true
order: 3
---
<div id="lookbook-container" class="grid">
{% for file in site.static_files %}
{% if file.path contains '/lookbook/thumbs/' %}
<div class="lookbook grid-item"><img src="{{file.path}}" /></div>
{% endif %}
{% endfor %}
</div>