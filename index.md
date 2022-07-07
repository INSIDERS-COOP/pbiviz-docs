---
---
You will find here all documents related to Insiders.coop Power BI Custom Visuals: the documentation of each visual and our [privacy terms]({{ '/privacy' | relative_url }}).

Here is a list of our visuals:
{% assign pages = site.pages | where_exp: "page", "page.customviz-doc == true" %}
{% for currentPage in pages %}
- [{{ currentPage.title }}]({{ currentPage.url | relative_url }})
{%- endfor %}

You can also find ways to contact us in the [contact page]({{ '/contact' | relative_url }}).