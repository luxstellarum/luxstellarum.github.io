---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: /
permalink: /
pagination: 
  enabled: true
---
<ul>
  {%- for post in paginator.posts -%}
  <li>
    {%- assign date_format = "%Y.%m.%d" -%}
    [ {{ post.date | date: date_format }} ] <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
  </li>
  {%- endfor -%}
</ul>