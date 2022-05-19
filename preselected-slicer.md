# Preseletected Slicer configuration

1. Put the dimension you want to slice on in the `Fields` bucket.
2. Put the column giving the pre-selections, related to the previously chosen dimension, in the `Pre Selection` bucket.
3. Drop in the `Dirty Status` bucket a column from the "technical" table.<br />
<u>This column must be unique for this Slicer instance!*</u>

*In order to make the `Dirty` status work across pages, each _Preselected Slicer_ instance needs its own "technical" column with two values `TRUE` and `FALSE`. We recommend to use only one "technical" table with one column per visual instance. Therefore, all boolean combinations need to appear in the dataset, as in the `_PreselectedSLicer` sample table.
{: class="footnotes"}