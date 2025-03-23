{% assign pages = site.pages | where_exp: "page", "page.customviz-doc == true" %}
{% for currentPage in pages %}
- [{{ currentPage.title }}]({{ '.' | append: currentPage.url }})
{%- endfor %}
