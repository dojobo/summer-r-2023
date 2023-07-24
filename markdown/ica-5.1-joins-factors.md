# ICA 5.1 joins and factors

Attach the tidyverse and medicaldata packages here:

``` r
library(tidyverse)
library(medicaldata)
```

Task 1 - INNER join

Consider the `medicaldata::theoph` data set, and suppose the PI gave us
access to the relational database where these records (and more) are
stored. Suppose also that some observations are incomplete, and we want
to retrieve and analyze only *complete* observations. Every valid
subject needs 1+ observations, and every valid observation needs a
subject.

\(1\) Run the code below to load CSV files. Examine each data frame. In
particular, run `dplyr::distinct(Subject)` to see the list of
distinct/unique subjects in each file.

``` r
# 😮‍💨
theoph_subjects <- read_csv("data/theoph_subjects.csv")
```

    Rows: 14 Columns: 3
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    dbl (3): Subject, Wt, Dose

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
theoph_observations <- read_csv("data/theoph_observations.csv")
```

    Rows: 143 Columns: 3
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    dbl (3): Subject, Time, conc

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

\(2\) If we inner-join these two tables, how many rows (rough estimate)
do you think will appear in the result? Which subjects will appear in
the result or not? Which observations will appear in the result or not?

\(3\) Use `dplyr::inner_join()` to join these tables by `Subject` and
assign the result to an object `theoph_joined`. How many rows and which
subjects appear in `theoph_joined` and why; were your predictions
correct?

``` r
# 😮‍💨
```

Task 2 - LEFT join

Consider the `medicaldata::laryngoscope` data set. We have many numeric
variables that represent categorical values. Let us perform joins to
replace the numeric values with human-readable ones.

\(1\) Run the code below to load CSV files. Examine each data frame.
These are our “lookup tables” or “value tables.”

``` r
# 🗣
lar_gender <- read_csv("data/lar_gender.csv")
```

    Rows: 2 Columns: 2
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr (1): Gender_label
    dbl (1): Gender

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
lar_mallampati <- read_csv("data/lar_mallampati.csv")
```

    Rows: 4 Columns: 2
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr (1): Mallampati_desc
    dbl (1): Mallampati_id

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

\(2\) Write code to use `dplyr::left_join()` to join `lar_gender` to
`laryngoscope` by `Gender` and then assign the result to a new object,
`lar_clean`. Before running the code, how many rows would you expect in
the result of a left join and why? Run the code and confirm that your
result has 99 rows, each with a readable gender.

``` r
# 🗣
```

\(3\) Perform another left join, this time between `lar_clean` and
`lar_mallampati`. Note that `lar_clean$Mallampati` corresponds to
`lar_asa$Mallampati_id`, so your `by` argument will need to be adjusted
accordingly.

``` r
# 🗣
```

Task 3 - OUTER (full) join

Returning to `theoph`, suppose you communicated with the PI that you
noticed the incomplete records in their database, and they asked you to
retrieve *all* records so that they can assess the situation. (For
example, there may have been a data entry error or a failed processing
script.)

\(1\) Reload the `theoph` CSVs from before and examine them again with a
full join in mind.

``` r
# 😮‍💨
theoph_subjects <- read_csv("data/theoph_subjects.csv")
```

    Rows: 14 Columns: 3
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    dbl (3): Subject, Wt, Dose

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
theoph_observations <- read_csv("data/theoph_observations.csv")
```

    Rows: 143 Columns: 3
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    dbl (3): Subject, Time, conc

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

\(2\) How many rows (roughly) do you expect to appear in the result and
why?

\(3\) Use `dplyr::full_join()` to combine these tables for the PI’s
review. Confirm that your result has **X** rows.

Task 4 - Visualize values as a factor

\(1\) Consider the `laryngoscope` plot below from a previous activity.
When you read the plot legend, how does Randomization appear to be
encoded? And what does `summary()` tell us about this vector?

\(2\) Mutate `Randomization` to convert it into a factor
(`as_factor()`); try to make better *labels* with a vector for the
`labels` argument (see `?factor`). `0` corresponds to “Standard
Macintosh \#4” and `1` corresponds to “AWS Pentaz Video.” Note the
result and store the result dataframe as `lar_clean2`. Run `summary()`
on `lar_clean2` to see how factor transformation has changed
`Randomization`.

(Note: in practice, there is no reason to make a new data frame, rather
than continue working with our previous `lar_clean` data. The data
frames are kept separate here only to simplify the assignment.)

\(3\) Recreate the plot in step 1 of this task (copy-paste if desired),
now using `lar_clean2`. Observe the difference in these plots (hint:
check the legend). What does the legend imply about the underlying data
in each case? Which plot is (therefore) better for our data?

Task 5 - Clean a factor

\(1\) Load the data below and consider the data frame `messy_bp`.
Convert `Race` to a factor (`mutate()` and `as_factor()`). What do you
notice about the levels of this factor?

\(2\) Inside of a `mutate()` call, use `forcats::fct_collapse()` and
`fct_recode()` to correct the levels of `Race`. Assign the result back
to `messy_bp`. Examine the data frame to ensure that your changes to
`Race` have taken effect.
