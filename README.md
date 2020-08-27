# CHANGEseq Replicate Analysis - Notes & Issues
__NOTE__ working from "summary_dev.Rmd"

# Issues

All 3 issues involve in counting occurrences across lab identifiers..

- 4.4.7 ~ line 456: instead of plotting read counts, want to plot occurrence - how many times that read count is seen in each off-target df, unique to NNN, unique to NSN, overlap of NNN-NSN, etc. We want to see given the off-target read count values, how are they distributed? And we want to make another version of this into a venn bar plot __NOTE__ I removed the y axis and the "stat = identity" and it resulted in this... 
  
- Venn Bar ~ line 486: I think the vennbar plot is again plotting based on readcounts which we don't want. We instead want off-target coordinates: Proportion of the amount of off-target sites that are unique to each lab combination and not the read counts. 
  
- Venn Bar Table ~ line 518: I can't figure out how to show this information properly but I think I need to first gather the correct data points in the above df
  
  
  
  
  
-----------------------------------------------------------------------------------------------------------------------------------
# For Sierra's Reference

-line 413: I stil ldon't understand the code to make paneled bar plots. Where do you define x and y? Metric and Value _ I need x = sub number and y = read count but paneled accroding to target site and lab as the 3 bars per plot... once that is done then the next item on this list is my next question
  __Response__ Use `facet_wrap` or `facet_grid` for panels https://ggplot2.tidyverse.org/reference/facet_grid.html
  
-line 353 how to change xy axis labels
  __Response__ You want to use the `labs` function, https://ggplot2.tidyverse.org/reference/labs.html. See line 368.