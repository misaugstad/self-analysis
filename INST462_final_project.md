Complementary stats for INST462 final project
================

NOTE: This is not the final project; we are creating an interactive infographic in Tableau. This document is meant to house the statistical analyses that accompany that infographic.

The value we want to predict is the productivity score that I gave myself each day, on a scale of 1 to 5. This is an ordinal value, so we would like to use an ordered logistic regression instead of a multinomial regression. To use this, we first need to test the proportional odds assumption.

We did not meet the proportional odds assumption (the code to find that is hidden, but I hope to show it later; on a deadline right now). Thus, we have to go with a multinomial regression. I binned the productivity score into &lt;=2, 3, and &gt;=4 so that there are more observations in each case.

Below is a table of the variables that had a p-values of less than 0.05, along with their odds ratios.

| variable       | productivity.rating | odds  | p.value | n   |
|:---------------|:--------------------|:------|:--------|:----|
| away.from.home | &gt;=4              | 0.325 | 0.033   | 102 |
| coding         | &lt;=2              | 0.411 | 0.004   | 285 |
| energy.rating  | &lt;=2              | 0.220 | 0.000   | 576 |
| energy.rating  | &gt;=4              | 3.368 | 0.000   | 576 |
| exhausted      | &lt;=2              | 0.352 | 0.000   | 248 |
| went.to.class  | &gt;=4              | 2.433 | 0.005   | 103 |
| worked.at.home | &lt;=2              | 0.520 | 0.040   | 351 |
