---
layout: page
title: /tags
permalink: /tags/
---
{%- for tag in site.tags -%}
  {%- assign tagName = tag | first-%}
  <h2>#{{tagName}}</h2>

  {%- assign relativePosts = tag | last-%}
  <ul>
  {%- for post in relativePosts -%}
    {%- assign date_format = "%Y.%m.%d" -%}
    <li>
    [ {{ post.date | date: date_format }} ] <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
    </li>
  {%- endfor -%}
  </ul>
{%- endfor -%}