---
layout: page
title:
permalink: /blog/art_capital2020/
---
Je partage ici mes coups de coeur lors de ma visite au Salon Art Capital 2020 au Grand Palais❤️!
<div>
{% for post in site.posts %}
{% if post.category contains 'art_capital2020' %}
    {% cycle 'add row' : '<div class="row">', '', '' %}
        <div class="column column-33">
            <div class="preview-panel">
                <a href="{{ post.url | prepend: site.baseurl }}">
                    <img src="{{ post.preview }}">
                </a>
                <div class="post-title">{{ post.title }}</div>
           </div>
        </div>
{% cycle 'end row' : '', '', '</div>' %}
{% endif %}
{% endfor %}
{% cycle 'end row' : '', '</div>', '</div>' %}
</div>

