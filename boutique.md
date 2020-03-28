---
layout: page
title: Boutique
permalink: /boutique/
---

<div>
{% for post in site.posts %}
{% if post.category contains 'boutique' %}
    {% cycle 'add row' : '<div class="row">', '', '' %}
        <div class="column column-33">
            <div class="preview-panel">
                <a href="{{ post.url | prepend: site.baseurl }}">
                    <img src="{{ post.preview }}">
                </a>
                <div class="post-title">{{ post.title }}
                <a href="#" class="tag">{{ post.price}}€ </a>
                <br>
                <a class="button" href="{{ post.url | prepend: site.baseurl }}">Acheter</a></div>
           </div>
        </div>
{% cycle 'end row' : '', '', '</div>' %}
{% endif %}
{% endfor %}
{% cycle 'end row' : '', '</div>', '</div>' %}
</div>