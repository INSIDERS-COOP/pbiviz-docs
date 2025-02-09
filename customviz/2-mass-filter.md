---
permalink: /mass-filter
title: Mass Filter
---
# Mass Filter
**Filter your Power BI reports instantly with a list of keywords and a copy/paste.**

Use the Mass Filter visual in your Power BI reports to filter other visuals with one of your dimensions and a set of keywords given by the user.

The advantage of the Mass Filter is that your users can copy a list of keywords from any external source (Excel, CSV, plain text file...), and paste it in the input box. When they click on the filter buttons, all values are used at once to filter the report instantly.

That's it! No intermediate steps needed.

The user can switch between inclusive (`In`) or exclusive (`NotIn`) filter by clicking on predefined button.

## Configuration
- Drop the column/measure you want to filter on in the _Field_ bucket.
- Set a maximum term limit if needed.
- Adjust formatting settings as desired.
- Adjust position and size of the visual on the report canvas.

The limit setting defaults to `0`, which disables the limit feature.<br />
By default there's no limit to the number of terms a user can use to filter a report.<br />
Be aware however that using a high number of filter terms may affect the performances of the report and even impact your global capacity.
{: class="note"}

## Usage
- Write or paste __keywords__ related to your dimension in the text area
- Click any filter button to filter the report on the matching elements.
- You can switch between include and exclude mode by clicking on the related filter button.

Keywords must be separated by commas or line breaks. Space will not be considered as a term separator.<br />
If your data contain commas or leading/trailing spaces or even line breaks (!!), you can use double quotes (") around an expression to escape these characters.
{: class="note"}

## FAQ

### Is there a limit to the number of keywords pasted in the search box?
No. We did not setup any limit by default. A user can potentially paste as much terms as they want, as far as there are no technical limit with an HTML textbox element or the number of filters a Power BI report can handle.

However, using a high number of filter may affect your report performances, and may even affect the global capacity.

To prevent unexpected behaviors, we recommend to use the limit setting in the format pane.

Note that duplicate terms in the list may be automatically removed after filter buttons are clicked.
{: class="note"}
