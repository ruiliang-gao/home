---
layout: default
title: Your New Jekyll Site
---

<div id="articles">
  <h1>Articles</h1>
  <ul class="posts noList">
    {%- for post in site.posts -%}
      <li>
      	<span class="date">{{ post.date | date_to_string }}</span>
      	<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      	<p class="description">{%- if post.description -%}{{ post.description  | strip_html | strip_newlines | truncate: 120 }}{%- else -%}{{ post.content | strip_html | strip_newlines | truncate: 120 }}{%- endif -%}</p>
        <p align="center">
        <iframe width="400" height="215" src="https://www.youtube.com/embed/uwlnJhhMKN4" title="TIPSlite usage and demo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </p>
      </li>
    {%- endfor -%}
  </ul>
</div>