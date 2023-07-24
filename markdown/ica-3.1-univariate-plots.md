# ICA 3.1 univariate plots

Attach the tidyverse and medicaldata packages here:

## Task 1 - Histograms

1)  Create a histogram of patient `BMI` in the `laryngoscope` data set.

``` r
# 🗣
# your code here 
```

2)  Note the visual output as well as the additional messages (one will
    be about bins). Modify your code from step 1 to add a `binwidth`
    argument with a value. Experiment until finding a good bin width for
    the data.

``` r
# 🗣
# your code here 
```

## Task 2 - Labels

1)  Write the code for a histogram of
    `laryngoscope$total_intubation_time` below.
2)  Now we want to modify the default axis and title labels. Run `?labs`
    to read about the `labs()` function. Jump down to the Examples to
    see how it is used.
3)  Use `labs()` to customize the x label to read “Total intubation time
    (seconds)”, and y to read “Count” (capitalized).

``` r
# 🗣
# your code here 
```

## Task 3 - Explore variables via histogram

Use `names()` and `geom_histogram()` to explore the distribution of
other numeric variables in `laryngoscope` and `polyps`.
