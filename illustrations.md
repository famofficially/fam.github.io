---
layout: page
title: Illustrations numériques
permalink: /arts_numeriques/illustrations/
---

<div>
{% for post in site.posts %}
{% if post.category contains 'illustrations' %}
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