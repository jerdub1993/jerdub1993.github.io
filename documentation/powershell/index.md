---
title: PowerShell Documentation
# layout: documentation_category
---
{% assign pages = site.pages
  | where_exp:"item", "item.path contains 'documentation/powershell/'"
  | where_exp:"item", "item.path != page.path" %}
{% for page in pages %}
- [{{ page.title }}]({{ page.url | absolute_url }})
{%- endfor %}