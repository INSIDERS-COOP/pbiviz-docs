---
permalink: /privacy
---
# Privacy Terms

INSIDERS.COOP Power BI visuals do not collect or use any of your personal information. Each visual only receives data from Power BI and does local computations and rendering in the client browser or desktop app. No information is transmitted to third-party services.

## List of our visuals
{% assign pages = site.pages | where_exp: "page", "page.customviz-doc == true" %}
{% for currentPage in pages %}
- [{{ currentPage.title }}]({{ currentPage.url | relative_url }})
{%- endfor %}