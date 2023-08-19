---
title: Documentation
layout: doc_base
---
{% assign pages = site.pages
    | where_exp:"item", "item.category contains 'doc_category'" %}
{%- if pages.size > 0 -%}
{% for indvpage in pages | sort title %}
## [{{ indvpage.title }}]({{ indvpage.url | absolute_url }})
{%- endfor %}
{%- endif -%}
