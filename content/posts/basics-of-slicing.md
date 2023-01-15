---
title: "Basics of Slicing Rows with Pandas"
date: 2022-11-17T16:08:51-05:00
draft: false
toc: false
images:
tags:
  - coding
  - data_science
  - rachel_grace_treene
  - python
  - pandas
---

Data scientists need to have a great understanding of slicing into dataframes because when working with large amounts of data, it's important to know how to select certain rows, columns, or cells. For example, when working with a big dataset of real estate sales in the last year, you might want to select only the first 100 rows, or only a few particular columns. This article will explain the basic syntax of slicing rows. To learn how to slice rows and columns at the same time, see my next article called 'Basics of Slicing Columns with Pandas.' To follow along with my code, you can copy and paste my code into the browser editor at the bottom of this page, or run on your machine.

For the purposes of this article, I'll be demonstrating slicing with the pandas dataframe built with the following code. Note that you will need to install pandas as pd for this code to run correctly:

{{< highlight python>}}
data = [['red', 22, 'round'], ['red', 2, 'square'], ['green', 5, 'round'], ['green', 31, 'square'], ['blue', 14, 'round'], ['blue', 12, 'square']]

df = pd.DataFrame(data, columns=['Color', 'Number', 'Shape'])

df
{{< /highlight>}}

The easiest way to take a slice of a dataframe is with brackets, []. This action selects rows of a dataframe based on what you put in the brackets. To select a single row, say the row at index value 3, you would run the following command:


{{< highlight python>}}
df[3:4]
{{< /highlight>}}

Notice that to display one row, I had to enter two values: 3 and 4, separated by a colon. Slicing typically requires 2 values. The first value, before the colon, represents the beginning index of the slice and is inclusive. The second value, after the colon, represents the ending index of the slice and is exclusive. So this slice only includes row 3.

A slice that would include multiple rows with the same kind of syntax could be called with the following code:

{{< highlight python>}}
df[2:5]
{{< /highlight>}}

This would return rows 2, 3, and 4.

If you want to select all rows up until a certain index, specify the exclusive ending index, but don't put anything for the beginning index, like so:

{{< highlight python>}}
df[:3]
{{< /highlight>}}

This will return rows 0, 1, and 2. To select all rows beginning at a certain index and all rows following, just do the opposite - specify the beginning index, but not the ending index:

{{< highlight python>}}
df[3:]
{{< /highlight>}}

This will return rows 3, 4, and 5.

There is a third dimension to slicing, which can select rows according to a specific pattern within the beginning and ending indices. To do this, add a third number to the slicing command, like so:

{{< highlight python>}}
df[1:5:2]
{{< /highlight>}}

Without the added 2, we would expect rows 1, 2, 3, and 4 to be selected. However, now that we've added the 2, the slicing command will select every other row within our specified range - that is, every 2 rows. So instead, we see rows 1 and 3. Here's another example:

{{< highlight python>}}
df[0:6:3]
{{< /highlight>}}

The beginning and ending indices alone would actually return the whole dataframe. But with the added 3, the command selects every 3 rows, so this command returns rows 0 and 3.

If we want to take every 3rd row from an entire dataframe, we don't have to specify the beginning and ending indices. Instead, we can run the following code:

{{< highlight python>}}
df[::3]
{{< /highlight>}}

This will give us what we want and is especially helpful when we're dealing with a bigger dataframe.

With all of these commands, if we use negative numbers the code runs similarly, with one catch: now, it considers the last row to be at index 0, and works backwards. It will return rows in reverse order, too. For example, if I slice the entire dataframe with the repeating pattern set to -1 (essentially, selecting all rows beginning with the end of the dataframe) I will return the dataframe with its rows in reverse order. The command would look like this:

{{< highlight python>}}
df[::-1]
{{< /highlight>}}

See 'Basics of Slicing Columns with Pandas' for taking slices that will specify rows and columns simultaneously.

Source: https://pandas.pydata.org/docs/user_guide/indexing.html

<script defer src="https://pyscript.net/alpha/pyscript.js"></script>
<link rel="stylesheet" href="https://raw.githubusercontent.com/Cat-Computing-Universe/PyLab/main/demo/demo.css" />
<script src="https://code.jquery.com/jquery-3.5.0.js"></script>
<py-env>
  - numpy
  - pandas
</py-env>
<b>pyscript REPL (numpy and pandas are installed)</b>
<br>
<div>
  <div>
    <py-repl id="my-repl" auto-generate="true" std-out="output" std-err="output">
import numpy as np
import pandas as pd
    </py-repl>
  </div>
  <div style="justify-content: right;display: flex;align-items: right;">
    <button class="button_reset" type="button">Clear Output</button>
  </div>
  <b>Output:</b>
  <div style="justify-content: center;display: flex;align-items: center;">
    <div id="output" style="width: 100%;margin: 2rem;"></div>
  </div>
  <script src="https://raw.githubusercontent.com/Cat-Computing-Universe/PyLab/main/demo/demo.js"></script>
</div>