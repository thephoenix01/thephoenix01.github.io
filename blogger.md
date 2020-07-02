---
layout: page
title: Blog Posts
identifer: blogpage
page-level: mainpage
permalink: blogs/
redirect_to: https://soumyadeepdas.gitlab.io/blogs/
---

<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ post.url | absolute_url }}">{{ post.title }}</a></h2>
      <p><span class="image left">
          
          <picture>
                <source data-srcset="{{ post.image-webp | absolute_url }}" type="image/webp" >
                <source data-srcset="{{ post.image | absolute_url }}" type="image/jpeg" > 
                <img src="{{ post.image-thumb | absolute_url }}" alt="{{ post.image-alt }}" data-src="{{ post.image | absolute_url }}"  class="lazyload" />
                </picture> 
      </span>{{ post.content | strip_html | truncatewords: 50 }}&nbsp;<a href="{{ post.url | absolute_url }}">(read more)</a></p>    
      <p><i class="fa fa-calendar"></i>&nbsp;&nbsp;<b>Published on :&nbsp;</b>{{ post.date | date: "%b %-d, %Y" }}</p>
      <hr>
    </li>
  {% endfor %}
</ul>