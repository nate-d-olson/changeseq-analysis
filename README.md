# CHANGEseq Replicate Analysis
-line 413: I stil ldon't understand the code to make paneled bar plots. Where do you define x and y? Metric and Value _ I need x = sub number and y = read count but paneled accroding to target site and lab as the 3 bars per plot... once that is done then the next item on this list is my next question
  __Response__ Use `facet_wrap` or `facet_grid` for panels https://ggplot2.tidyverse.org/reference/facet_grid.html
  
-line 353 how to change xy axis labels
  __Response__ You want to use the `labs` function, https://ggplot2.tidyverse.org/reference/labs.html. See line 368.

__NOTE__ working from "summary_dev.Rmd"
# Issues

- reading in data ~ line 204: when I have replicate number string with NNN2 I have a leading underscore.  I can’t just remove based on index of character because the position of the string I want to capture shifts when i’m dealing with the replicate string. So how do I remove this leading underscore only when I have this replicate NNN2 string?

- 4.3 Table ~ line 340: can we limit the decimal places shown in the ratio columns? Do we do this at the calculation step, gather step, or writing step?

- 4.4.7 ~ line 508: instead of plotting read counts, want to plot occurrence - how many times that read count is seen in each off-target df, unique to NNN, unique to NSN, overlap of NNN-NSN, etc. I thought we did this? Was it not committed? Also instead of plotting it like bar plots, Samantha was interested it plotting it like the Venn Bar plots below. We want to see given the off-target read count values, how are they distributed? Also want to do something else but see point below as we also want to do it to the venn bar plot next.

- 4.5: We've determined that bioinformatics isn't a factor so we want to remove NSS and any NSS overlaps from this comparison to make this easier to read. It may make some of this easier to see as well. FOr example, we couldn't tell if there were a bit of blue between the purple and green for A-E. I added a filter line to 547 but some combinations of NSS are still showing in the plot. When I try to filter in other lines, the I then get errors with the group by function... is there an easier way to do this at the beginning to remove NSS completely?



  