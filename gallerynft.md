---
layout: page
title:
logo: logoblack
permalink: /gallery/nft

---

<nav class="navbarshop">

<ul>
      <li class="nav-item">
        <a href="{{ site.baseurl }}/gallery/">All</a>
       
      </li>
      <span aria-hidden="true" style="color: grey">|</span>
      <li class="nav-item">
        <a href="{{ site.baseurl }}/gallery/gallerydigitalart">Digital Art</a>
       
      </li>
       <span aria-hidden="true" style="color: grey">|</span>
      <li class="nav-item"><a href="{{ site.baseurl }}/gallery/gallerytraditionalart">Traditional Art</a>
      </li>
      
       <span aria-hidden="true" style="color: grey">|</span>
      <li class="nav-item"><a href="{{ site.baseurl }}/gallery/nft">NFT</a>
      </li>
      
    </ul>
  </nav>
  
<div>

{% for post in site.posts %}
{% if post.category contains 'nft' 
%}
    {% cycle 'add row' : '<div class="row">', '', '' %}
        <div class="column column-33">
            <div class="preview-panel">
                <a href="{{ post.url | prepend: site.baseurl }}">
                    <img src="{{ post.preview }}">
                </a>
                <div class="post-title">{{ post.title }}</div>
               {% if post.tagmerit %}
                <a href="#" class="tag" style="font-size: 9px;">{{post. tagmerit}}</a>
                {% endif %}
           </div>
        </div>
{% cycle 'end row' : '', '', '</div>' %}
{% endif %}
{% endfor %}
{% cycle 'end row' : '', '</div>', '</div>' %}
</div>