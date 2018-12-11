
<!-- README.md is generated from README.Rmd. Please edit that file -->

# jl12: Johnson-Laird’s (2012) Tonal Dissonance Model

[![lifecycle](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)

The `jl12` R package implements Johnson-Laird’s (2012) tonal dissonance
model.

## Installation

Within R, you can install the current version of `jl12` from Github as
follows:

``` r
if (!require(devtools)) install.packages("devtools")
devtools::install_github("jl12")
```

## Usage

Higher scores correspond to greater dissonance. These scores correspond
to each of the distinguishable categories in the cultural component of
Johnson-Laird et al.’s (2012) algorithm.

Major chord:

``` r
library(jl12)
jl_tonal_dissonance(c(0, 4, 7))
#> [1] 1
```

Minor chord:

``` r
jl_tonal_dissonance(c(0, 3, 7))
#> [1] 3
```

Cluster chord:

``` r
jl_tonal_dissonance(c(0, 1, 2))
#> [1] 12
```

The model comprises several rules. It is possible to call these rules
individually, for example:

``` r
jl_rule_1(c(0, 3, 7))
#> [1] 1
jl_rule_2(c(0, 3, 7))
#> [1] TRUE
jl_rule_3(c(0, 3, 7))
#> [1] FALSE
#> attr(,"solution")
#> [1]  0  3  7 10
```

## References

Johnson-Laird, P. N., Kang, O. E., & Leong, Y. C. (2012). On musical
dissonance. Music Perception, 30(1), 19–35.
