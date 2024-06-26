---
permalink: /mass-filter
title: Mass Filter
---
# Mass Filter
**Filter your Power BI reports instantly with a list of keywords and a copy/paste.**

Use the Mass Filter visual in your Power BI reports to filter other visuals with one of your dimensions and a set of keywords given by the user. The advantage of the Mass Filter is that your users can copy a list of keywords from any external source (Excel, CSV, plain text file...), and paste it in the input box. When they click on the filter button, all values are used at once to filter the report instantly. No intermediate steps needed. The user can alternate between inclusive or exclusive filter with a click on a button.

## Configuration
Put the dimension you want to filter on in the Fields bucket.<br />
You can change a few settings in the Format option tab.<br />
Adjust position and size of the visual on the report canvas.

## Usage
Write or paste __keywords__ related to your dimension in the text area.<br />
Click the filter button to filter the report on the matching elements.<br />
You can switch to exclude mode by clicking on the filter mode button.

Keywords must be separated by commas or line breaks.<br />
If your data contain commas or leading/trailing spaces, you can put a keyword between "double quotes".
{: class="note"}

## FAQ

### Is there a limit to the number of keywords pasted in the search box?
No. We didn't setup any limit.
You can potentially paste as much terms as you want, as far as there are no technical limit with an HTML textbox element.

However, if there are duplicates in your list, they will be automatically removed after setting the filters.
