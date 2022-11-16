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

{{< image src="C:\Users\Rachel\Pictures\Engagement_Photos\highlights\rachel-and-will-engagement.jpg" alt="Picture from photoshoot" position="center" style="border-radius: 8px;" >}}

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