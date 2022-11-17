---
title: "Examplepost"
date: 2022-11-11T12:10:00-05:00
draft: false
toc: false
images:
tags:
  - untagged
---

Hello! Here is the first ever post on datascienceforbabies.com!!

![Yellow Duck](/pexels-photo-268533.webp 'Yellow Duck')

Above is a test of inserting an image.

``` html
  # break dataframes into test and training - this way the test data is completely new (80/20 split)
  aqu_train =  aqu.sample(frac=0.8, random_state=25)
  aqu_test = aqu.drop(aqu_train.index)
  bel_train = bel.sample(frac=0.8, random_state=25)
  bel_test = bel.drop(bel_train.index)
  sar_train = sar.sample(frac=.8, random_state=25)
  sar_test = sar.drop(sar_train.index)
```

Above is a test of inserting code.

<script defer src="https://pyscript.net/alpha/pyscript.js"></script>
<link rel="stylesheet" href="https://raw.githubusercontent.com/Cat-Computing-Universe/PyLab/main/demo/demo.css" />
<script src="https://code.jquery.com/jquery-3.5.0.js"></script>
<py-env>
  - numpy
</py-env>
<b>pyscript REPL (numpy is installed)</b>
<br>
<div>
  <div>
    <py-repl id="my-repl" auto-generate="true" std-out="output" std-err="output">
import numpy as np
print("Hello, world!")
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

Above is a test of inserting runnable code.

{{< highlight python>}}
print("Hello, world!")
{{< /highlight >}}

Above is a test of inserting highlighted code.