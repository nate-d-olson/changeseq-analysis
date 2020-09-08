# CHANGEseq Replicate Analysis - Notes & Issues
__NOTE__ working from "summary_dev.Rmd"

# Issues

- I keep forgetting to ask what the "; packageVersion("here")" portio of the "library(here); packageVersion("here")" does?

-
  
-----------------------------------------------------------------------------------------------------------------------------------
# For Sierra's Reference

-line 413: I stil ldon't understand the code to make paneled bar plots. Where do you define x and y? Metric and Value _ I need x = sub number and y = read count but paneled accroding to target site and lab as the 3 bars per plot... once that is done then the next item on this list is my next question
  __Response__ Use `facet_wrap` or `facet_grid` for panels https://ggplot2.tidyverse.org/reference/facet_grid.html
  
-line 353 how to change xy axis labels
  __Response__ You want to use the `labs` function, https://ggplot2.tidyverse.org/reference/labs.html. See line 368.