# Summer R learning materials

These materials were developed and presented for the Summer R series at the University of Pittsburgh's Physician Scientist Training Program.

The repository is organized as follows:

| Directory    | Contents |
| --- | --- |
| `homework/`  | Homework assignments (currently there are two), Quarto notebooks   |
| `ica/`       | In-class assignments, Quarto notebooks                             |
| [`markdown/`](https://github.com/dojobo/summer-r-2023/tree/main/markdown)  | [Markdown and PDF versions of materials for easy browsing on GitHub](https://github.com/dojobo/summer-r-2023/tree/main/markdown) |
| `sessions/`  | Materials collocated according to each session                     |
| `slides/`    | Presentation slides, written as Quarto notebooks and revealjs html |

Most example data come from the [{medicaldata}](https://higgi13425.github.io/medicaldata/) package.

## Syllabus

This course is an introduction to R (specifically the tidyverse) from zero using medical data examples.

### Learning goals

1.  Transfer tabular data into and out of R
2.  Examine and make sense of data (at the level of descriptive statistics)
3.  Visualize data according to what kind of data you have, and what you want to show
4.  Manipulate and restructure data so that it can be analyzed (also called "data cleaning")
5.  Write reproducible cleaning tasks, analyses, and plots for sharing with colleagues (and your future self)
6.  Utilize R documentation to solve problems and explore possibilities
7.  Gain an understanding of the R packages ecosystem

### Session format

Each 2-hour class session is broken into 2-3 segments. For each segment, the instructor briefly presents information and one or more examples, using the slides. Then students work alone or in small groups on related in-class activities (ICAs), for which solutions are provided to check their own work. The instructor is available during the ICAs to answer questions and help solve technical issues. The instructor may cut short the ICA period as needed in order to reach the next segment. Unfinished ICAs may be further explored individually after class.

### Schedule and topics studied

| Session  | Topics | Links |
| --- | --- | --- |
| 1 | RStudio orientation; using R for simple calculations; loading and saving data; data types and structures; R packages; R notebooks. | [slides](https://github.com/dojobo/summer-r-2023/blob/main/markdown/slides-session-1.pdf), [ICA 1.1](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica-1.1-console-calculations.md), [solutions 1.1](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica_solns/ica-1.1-solns.pdf), [ICA 1.2](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica-1.2-loading.md), [solutions 1.2](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica_solns/ica-1.2-solns.pdf) |
| 2 | Working with data frames: descriptive statistics; filtering and sorting; selecting and ordering variables; grouping. Data viz: base R plots (histogram, bar, scatter). | [slides](https://github.com/dojobo/summer-r-2023/blob/main/markdown/slides-session-2.pdf), [ICA 2.1](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica-2.1-pipes-select-sort.md), [ICA 2.2](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica-2.2-filter-summarize-group.md), [solutions 2.1](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica_solns/ica-2.1-solns.pdf), [solutions 2.2](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica_solns/ica-2.2-solns.pdf) |
| 3 | Data viz: ggplot2 and the grammar of graphics, common plots. Rendering notebooks to different formats. | [slides](https://github.com/dojobo/summer-r-2023/blob/main/markdown/slides-session-3.pdf), [ICA 3.1](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica-3.1-univariate-plots.md), [ICA 3.2](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica-3.2-multivariate-plots.md), [solutions 3.1](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica_solns/ica-3.1-solns.pdf), [solutions 3.2](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica_solns/ica-3.2-solns.pdf) |
| 4 | Handling missing data; adding new variables to a data frame; joining tables. Time permitting: working with dates; working with string data. Data viz: missingness; faceting (small multiples). | [slides](https://github.com/dojobo/summer-r-2023/blob/main/markdown/slides-session-4.pdf), [ICA 4.1](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica-4.1-missing-data.md), [ICA 4.2](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica-4.2-new-vars-faceting.md), [solutions 4.1](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica_solns/ica-4.1-solns.pdf) |
| 5 | Handling categorical variables (recoding and reordering); pivoting columns and rows; checking a variable for Normality; introductory inference. Data viz: output options and image formats; annotations; Q-Q plots. | [slides](https://github.com/dojobo/summer-r-2023/blob/main/markdown/slides-session-5.pdf), [ICA 5.1](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica-5.1-joins-factors.md), [ICA 5.2](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica-5.2-pivoting.md), [ICA 5.3](https://github.com/dojobo/summer-r-2023/blob/main/markdown/ica-5.3-inference-modeling.md) |

These materials are licensed for reuse under a [CC BY-NC (Attribution-NonCommercial) 4.0 International license](https://creativecommons.org/licenses/by-nc/4.0/).
