---
layout: page
title:
permalink: /arts_numeriques/posters/
---
L'ensemble des posters réalisés numériquement pour participer au concours d'affiches de différents festivals et carnavals organisés chaque année en France.
<div>
{% for post in site.posts %}
{% if post.category contains 'posters' %}
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