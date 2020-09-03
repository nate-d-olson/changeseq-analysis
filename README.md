# CHANGEseq Replicate Analysis - Notes & Issues
__NOTE__ working from "summary_dev.Rmd"

# Issues

- line 561 - for the venn df table, is there an easy way to show these values as percentages across the row? I was going to mutate, sum the row and then calculate each col but there may be an easier way that I don't know of. Here is a screen shot of the table in question: Each row is a target site and the row will be equal to 100, each col will need to be divided by that sum. 

![table](/Users/sdm8/Desktop/changeseq-analysis/Screen Shot 2020-09-03 at 10.19.12 AM.png)



- dfs starting at line 603 are not working correctly. When I pivot:

```{r}
nsn1_v_nnn1 <- summary_df %>% 
    filter(!Site_Substitution_Number == 0) %>%
  select(Chromosome, Start, End, 'Genomic Coordinate', Nuclease_Read_Count, Site_Sequence,
         Site_Substitution_Number, Site_Sequence_Gaps_Allowed, lab, changeseq_run, target_site, 
         Sub_Only, Indel_Only, Sub_or_Indel) %>%
  pivot_wider(names_from = "lab", values_from = "Nuclease_Read_Count", values_fill = 0)
```

The only count info transferring is for labs NNN1 & NNN2 but does eventually shift when you start scrolling down far enough through the df. It's like it isn't resolving it to that level? It could be that there is just simply no overlap  but I find it unlikely. 
  
  
  
-----------------------------------------------------------------------------------------------------------------------------------
# For Sierra's Reference

-line 413: I stil ldon't understand the code to make paneled bar plots. Where do you define x and y? Metric and Value _ I need x = sub number and y = read count but paneled accroding to target site and lab as the 3 bars per plot... once that is done then the next item on this list is my next question
  __Response__ Use `facet_wrap` or `facet_grid` for panels https://ggplot2.tidyverse.org/reference/facet_grid.html
  
-line 353 how to change xy axis labels
  __Response__ You want to use the `labs` function, https://ggplot2.tidyverse.org/reference/labs.html. See line 368.