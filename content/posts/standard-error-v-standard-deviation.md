---
title: "Standard Error v. Standard Deviation"
date: 2022-11-16T13:03:20-05:00
draft: false
toc: false
images:
tags:
  - statistics
  - data_science
  - eve_schoenrock
---
What's the difference between standard error and standard deviation? Every new data scientist asks this question of themselves. Honestly, the difference is nuanced, and standard error is a form of standard deviation.

Standard Deviation is a measure of the variability within a sample - this can be a sample of a population or the entire population itself. A lower standard deviation indicates that values in a distribution tend closer toward the mean of that distribution, while high standard deviation suggests that values are dispersed more greatly from the mean. 

Standard Error is used in reference to variability across sample distributions. If you were to draw infinite repeated samples from the original population and take the mean of each sample, the standard deviation on the distribution of those sample means combined is the standard error. We compute the standard error as: 
```html
standard_deviation/sqrt(sample_size)
```
The standard error on an estimation reflects how greatly that estimate varies under repeated sampling, which is why it is often used in the computation of confidence intervals. That being said, the 95% confidence interval on an estimate is calculated by:
``` html
confidence_interval = [estimate - 2*standard_error(estimate), estimate + 2*standard_error(estimate)]
```
Most frequently, data scientists retrieve the value of standard_error(estimate) from the model output.

By Eve Schoenrock