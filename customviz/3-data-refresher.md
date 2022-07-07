---
permalink: /data-refresher
title: Data Refresher
---
# Introduction
**Visual that repeatedly refreshes data, with a fixed time delay between each refresh.**

Use the Data Refresher visual on your reports to repeatedly update the data and the other visuals. It is particularly useful when you display your dashboard on a TV screen without input devices and you want to see the latest fresh data.

# Data Refresher configuration
Put a __dummy*__ dimension in the _Whatever_ bucket field.<br />
Set the desired refresh rate in the _Format_ option tab.<br />
You can change the text size and the template of the label if needed.<br />
Adjust position and size of the visual on the report canvas.

# Usage
Click on the button to start/stop the refresh loop.

# Template placeholders
- `{refreshRate}`: Displays the current refresh rate - "n units"
- `{lastRefresh}`: Displays the date and time of the last data refresh made by the visual.

*The Data Refresher uses a dimension to loop over its values to set a filter in order to trigger update on other visuals. To make this filter "transparent" to other visuals, make sure to add a dummy column to iterate on.
{: class="footnotes"}
