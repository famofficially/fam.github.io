---
layout: page
title: Shop
logo: logoblack
permalink: /shop/
---
<nav class="navbarshop">

<ul>
      <li class="nav-item">
        <a href="{{ site.baseurl }}/shop/">All</a>
       
      </li>
      <span aria-hidden="true" style="color: grey">|</span>
      <li class="nav-item">
        <a href="{{ site.baseurl }}/shop/shopprints">Prints</a>
       
      </li>
       <span aria-hidden="true" style="color: grey">|</span>
      <li class="nav-item"><a href="{{ site.baseurl }}/shop/shoporiginals">Originals</a>
      </li>
      
      <span aria-hidden="true" style="color: grey">|</span>
      <li class="nav-item">
        <a href="{{ site.baseurl }}/shop/shopnft">NFT</a>
       </li>
      
    </ul>
  </nav>


<div>
{% for post in site.posts %}
{% if post.category contains 'shopprint' or 
      post.category contains 'shoporiginal'
%}
    {% cycle 'add row' : '<div class="row">', '', '' %}
        <div class="column column-33">
            <div class="preview-panel">
                <a href="{{ post.url | prepend: site.baseurl }}">
                    <img src="{{ post.preview }}">
                </a>
                <div class="post-title">{{ post.title }}
                <br>
                <a href="#" class="tag">{{ post.price}}€ </a>
                <br>
                <a class="button" href="{{ post.url | prepend: site.baseurl }}">Buy</a></div>
           </div>
        </div>
{% cycle 'end row' : '', '', '</div>' %}
{% endif %}
{% endfor %}
{% cycle 'end row' : '', '</div>', '</div>' %}
</div>
**Other SHOPs**<br>
[▸ Etsy shop ](https://www.etsy.com/fr/shop/famofficially)
