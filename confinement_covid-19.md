---
layout: page
title:
permalink: /blog/confinement_covid-19/
---
Dessins ont été réalisés dans la période de confinement covid-19 en mars 2020.
<div>
{% for post in site.posts %}
{% if post.category contains 'confinement_covid-19' %}
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

