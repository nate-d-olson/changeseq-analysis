2020-08-04

In the tidy_replicate_analysis.Rmd file: 

Specific things to call attention to:

-line 413: I stil ldon't understand the code to make paneled bar plots. Where do you define x and y? Metric and Value _ I need x = sub number and y = read count but paneled accroding to target site and lab as the 3 bars per plot... once that is done then the next item on this list is my next question

-line 395 & 403: same plots but one is scatter and other is bar. I need to find a way to plot the indel_only read counts and sub_or_indel read counts. Prior, I was giving it a sub number of 10 and 11 in order to plot it on the same graph and just defining it that way in the legend.

-line 353 how to change xy axis labels

- line 496: This is not complete and I can't really figure out how to do it the tidy way. I need to tally each time a genomic coordinate is and isnt shared between labs in a pairwise fashion. I am kind of there but I need to 1) alter or add another if_else statement  - the way I have it now is like or but I think that it should be maybe case_when so I can write something like "if is.na(NSN) == FALSE & is.na(NNN) == TRUE" blah Idk everytime I start to think about it it's like a really large set of code. Then to summarise I'll need to tally the NSN unique, NNN unique and NSN_NNN overlap column.  

- line 574: I'm passing all 3 plots but it's just repeating the first one 3 times -- "Paneled view of pairwise lab comparisons of all off-target genomic coordinates and their respective read counts."

__NEXT STEPS__

- For each target site, record the unique read count value across labs and then tally how many times that read count appears in the off-target data frame
- uploading two excel files that Samantha has done additional work with. She would like for us to include these calculations. 
  * The "Summary" tab in the "Fig1i_A-F_Plots_SM split plots" workbook 
  & 
  * The "Summary 1-12" & "Summary A-F" in the "Replicate Stats_St. Jude 1-12_A-F" workbook. 
  
  She did say:
  
  > the calculations and information may not be obvious and I was still adding ideas as to what might be useful to calculate.
  
  So if we need to disuss things with her, I can do that on our Tuesday meeting