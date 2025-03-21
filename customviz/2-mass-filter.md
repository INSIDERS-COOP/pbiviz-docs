---
permalink: /mass-filter
title: Mass Filter
---
# Mass Filter
**Filter your Power BI reports instantly with a list of keywords and a copy/paste.**

Use the Mass Filter visual in your Power BI reports to let users filter other visuals on one of your columns/measures with a list of keywords.

The advantage of the Mass Filter is that your users can copy a list of keywords from any external source (Excel, CSV, plain text file...), and paste it in the input box. When they click on the filter buttons, all values are used at once to filter the report instantly.

That's it! No intermediate steps needed.

The user can switch between inclusive (`In`) or exclusive (`NotIn`) filter by clicking on predefined button.

## Configuration
- Drop the column/measure you want to filter on in the _Field_ bucket.
- Set a maximum term limit if needed.
- Adjust formatting settings as desired.
- Adjust position and size of the visual on the report canvas.

### Max Term Limit
There is a new _Limit_ setting in the format pane, which allows to set a maximum number of terms a user can paste in the filter box.

The limit setting defaults to `0`, which disables the whole feature.<br />
By default there's no maximum number of terms a user can use to filter a report.

Be aware however that using a high number of filter terms may affect the performances of the report and even impact your global capacity.
{: class="note"}

When set to a number grater thant `0`, the limit is active and a user won't be able to filter the report with more terms than the number set in the format pane.

Setting a limit unhides another new setting to enable or diable the status bar.<br />
When enabled, a status bar will show above or below the filter box in the visual displaying the current amount of terms in it, as well as the maximum number of terms available.

A new formatting panel will also appear to modify the appearance of the status bar.

As formatting settings, all of these won't be synchronized between pages.<br />
Pay attention when you change the configuration on synchronized filters.
{: class="note"}

### Cross Page Synchronization
The _Mass Filter_ can now be synchronized between pages like any other slicer.

Just open the synchronization panel and select the pages on which you want the filter to appear and be synchronized.

As formatting settings aren't synchronized between pages, we suggest to configure your filter on the first page on which you want it to appear, then synchronize it with the synchronization panel and let Power BI duplicate it on selected pages.

Once synchronized and configured, each visual on each page will behave as a standalone visual, unless for the filters which will synchronize.<br />
If you modify any setting from the format pane, you will need to manually replicate the change on every page the visual is synchronized on.

You will encounter incoherent behavior when synchronized _Mass Filter_ visuals don't share the same maximum term limit.<br />
If a user uses the maximum number of terms available in the visual configured with the higher limit, the visuals with lower limits on other pages will be in error state, and therefore unusable.
{: class="note"}

## Usage
- Write or paste __keywords__ related to your dimension in the text area
- Click any filter button to filter the report on the matching elements.
- You can switch between include and exclude mode by clicking on the related filter button.

Keywords must be separated by commas or line breaks. Space will not be considered as a term separator.<br />
If your data contain commas or leading/trailing spaces or even line breaks (!!), you can use double quotes (") around an expression to escape these characters.
{: class="note"}

## Migration 2.2.7.1 => 3.0.0.1
The version 3 of the Mass Filter custom visual is a breaking change.

The capabilities of the visual have changed and, for better naming consistency, the name of the bucket field has been modified.

It results in the need to **reconfigure** the visual by **removing and dropping again the column/measure used in the bucket field**.

Unfortunately, if you used the Mass Filter visual in one of your reports, it will automatically update from the App Source as soon as it will be available to you.

The Power BI platform doesn't leave the choice of which version you'd like to use. Moreover, the version on the App Source prevails on an eventual version you might have in your organization, which also prevails on an eventual local file you'd like to use.

## FAQ

### Is there a limit to the number of keywords pasted in the search box?
No. We did not setup any limit by default. A user can potentially paste as much terms as they want, as far as there are no technical limit with an HTML textbox element or the number of filters a Power BI report can handle.

However, using a high number of filter may affect your report performances, and may even affect the global capacity.

To prevent unexpected behaviors, we recommend to use the limit setting in the format pane.

Note that duplicate terms in the list may be automatically removed after filter buttons are clicked.
{: class="note"}

## Changelog
### 3.0.0.1
**Features**
- Added limit setting and related formatting options.
- Added cross-page synchronization.
- Changed UI/UX for better consistency and intuitiveness.

**Bug fix**
- Separator chars (`,` and `LF`) escaping with double quotes (`"`) now fully functionnal.