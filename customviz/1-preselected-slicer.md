---
permalink: /preselected-slicer
title: Preselected Slicer
---
# Introduction

**The Preselected Slicer is a slicer for Power BI where values can be pre-selected by your data.**

Use the Preselected Slicer in your Power BI reports to filter other visuals with one of your dimensions, like with a regular slicer. The advantage of the Preselected Slicer is that you can use another column or measure to tell which values must be pre-selected when a user opens the report. Then, instead of modifying the report each time you need to change the default selection, the model will tell the Preselected Slicer which is the default selection. Let's say you have a report with different visuals. You would like to display your charts filtered by the current year or month by default. You can do that with the Preselected Slicer. Your users will still be able to filter on other years or months by changing the current selection. Note: The Preselected Slicer needs a third "technical" measure in order to keep its dirty status updated cross pages.

# Preseletected Slicer configuration

1. Put the dimension you want to slice on in the `Fields` bucket.
2. Put the column giving the pre-selections, related to the previously chosen dimension, in the `Pre Selection` bucket.
3. Drop in the `Dirty Status` bucket a column from the "technical" table.<br />
<u>This column must be unique for this Slicer instance!*</u>

*In order to make the `Dirty` status work across pages, each _Preselected Slicer_ instance needs its own "technical" column with two values `TRUE` and `FALSE`. We recommend to use only one "technical" table with one column per visual instance. Therefore, all boolean combinations need to appear in the dataset, as in the `_PreselectedSLicer` sample table.
{: class="footnotes"}
