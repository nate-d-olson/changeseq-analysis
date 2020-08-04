2020-08-04

In the tidy_replicate_analysis.Rmd file: 

Line 175 is where I picked up. 

Specific things to call attention to:

- line 206: not sure how to code the bar plot. Want to show all 3 summarise variables separated by target site and lab
- line 219: How do I now subset the df to consider only the top 25% of off-target read counts?
- line 235: since I'm piping into this command, how do I reference the first row$Nuclease_Read_Count of the df?
- line 251: I'm not doing something correctly here. Want to have bins for 1-6 mismatches and group by target site, lab