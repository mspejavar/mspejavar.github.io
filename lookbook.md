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
<script>
    var $grid = $('.grid').imagesLoaded( function() {
        // init Packery after all images have loaded
        $grid.packery({
            itemSelector: '.grid-item',
            gutter: 0
        });
    });
    $(".grid-item").hover(function() { // Mouse over
        $(this).siblings().stop().fadeTo(300, 0.5);
        $(this).parent().siblings().stop().fadeTo(300, 0.2); 
    }, function() { // Mouse out
    $(this).siblings().stop().fadeTo(300, 1);
    $(this).parent().siblings().stop().fadeTo(300, 1);
});
</script>