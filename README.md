2020-08-04

In the tidy_replicate_analysis.Rmd file: 

Specific things to call attention to:

- line 284: would a different kind of graph be better? Probably but I need to think about it. We can chat about plotting next week. *sounds good*
- line 330: how do I make a plot similar to that on line 288-303 where each panel has a sample and x axis has substitution number. I don't think I'm understanding the code in that plot.  - Added the plot I think you were looking for. *yes- can you explain the facet_wrap line when we meet next?*

Wrote chunk for the summary table starting on line 361
-For this, is there a better way to...
1. Combine specific columns of data frames in one chunk without having to make multiple variables? Can I have it like this with the multuple merge() functions but just pipe so that one variable is being made and I'm piping 3 times?
2. Up until I combine the final df (substitution_count_df, line 378), each changeseq_run row is unique. However, this column reports the number of substitutions, unique for each sample. So one sample can now have multiple rows of the same information up until this column. Is there a better way to incorporate this information? Perhaps as columns rather than rows? 

For instance.. 

Instead of: 

changeseq_run     | <.....> | Site Subsitution Number | Substitution Read Count
------------------|---------|-------------------------|-------------------------
NNN_A_CCR5_site_3 |         | 1                       | 210         
NNN_A_CCR5_site_3 |         | 3                       | 112
NNN_A_CCR5_site_3 |         | 4                       | 542
NNN_A_CCR5_site_3 |         | 5                       | 790
NNN_A_CCR5_site_3 |         | 6                       | 962

we have something like this:

changeseq_run     | <.....> | sub_number_1_readcount | sub_number_2_readcount | sub_number_3_readcount | sub_number_4_readcount | sub_number_5_readcount| sub_number_6_readcount
------------------|---------|------------------------|------------------------|------------------------|------------------------|-----------------------|-----------------------
NNN_A_CCR5_site_3 |         | 210                    | 0                      | 112                    | 542                    | 790                   | 962     

We'll probably have to tweak the table generation code?