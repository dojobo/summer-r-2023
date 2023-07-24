# ICA 4.2 New variables, faceting

Attach the tidyverse and medicaldata packages here:

``` r
library(tidyverse)
library(medicaldata)
```

#### Task 1 - Calculate a column

1)  In `medicaldata::smartpill`, use `dplyr::mutate()` to calculate a
    new `BMI_metric` variable, using `Height` and `Weight`. Make mental
    note of the units involved (`?smartpill` may help). Assign the
    result to a new object called `sp`.

``` r
# 💊
```

2)  Let’s try converting these variables to English units. In `sp`,
    mutate new `Height_in` and `Weight_lbs` columns, using the existing
    data as basis. Make sure to store the successful result back into
    `sp`.

<!-- -->

3)  Mutate a new `BMI_english` column using the English-converted units
    from step 2. Use `dplyr::select()` to easily compare your two BMI
    calculations side by side.

#### Task 2 - Inclusion criterion

1)  After consulting the polyps experimental protocol, you find that
    patients must participate in the full 12 months in order to be
    included in the analysis. The PI would like you to create a new
    logical (T/F) variable called `inclusion`. Check whether `number12m`
    is `NA` or not, and calculate an appropriate T/F value for each
    patient. Assign the successful result to a new object `pol`.

2)  Filter `pol` for cases to include, based on the new `inclusion`
    column.

``` r
# 🅿
```

#### Task 3 - Age groups

1)  Use numeric and visual summary function(s) to see what the spread of
    ages is in `smartpill`. (Hints: `summary()`,
    `ggplot2::geom_histogram()`, `hist()`)

2)  Suppose we want to establish a new variable called `age_group`.
    Using `mutate()` and `case_when()`, assign each patient to the
    appropriate ranged group: 0-30, 31-40, 41-50, 51-100. Assign the
    successful result to `sp`. (Note: if you use `smartpill`, rather
    than `sp` from previous exercise, as starting point to do this work,
    you will overwrite the recent columns!)

3)  Use `group_by()` and `summarize()` to see how many patients are in
    each age group. Does this seem roughly congruent with what you saw
    in step 1?

``` r
# 💊
```
