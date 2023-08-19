---
title: PowerShell Documentation
# layout: documentation_category
---
{% assign pages = site.pages
  | where_exp:"item", "item.path match 'documentation/powershell/[^$]'" %}
{% for page in pages %}
- [{{ page.title }}]({{ page.url | absolute_url }})
{%- endfor %}