---
title: Documentation
layout: documentation_base
---
{% assign pages = site.pages
    | where_exp:"item", "item.category contains 'documentation_category'" %}
{%- if pages.size > 0 -%}
{% for indvpage in pages | sort %}
## [{{ indvpage.title }}]({{ indvpage.url | absolute_url }})
{%- endfor %}
{%- endif -%}
