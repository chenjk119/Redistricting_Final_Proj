# Redistricting_Final_Proj

## Table of Contents

## Gathering and Cleaning of data
[LA_MAUP.ipynb](LA_MAUP.ipynb) <br>

## Short Burst
[short_burst_run.ipynb](short_burst_run.ipynb) <br>
updater: 
- population
- black
- cut edges

For congressional districts: <br>
gingles = Gingleator(init_partition, pop_col="TOTPOP", threshold=0.1, score_funct=None, epsilon=0.05, minority_perc_col="NH_BLACK_perc") <br>
where Gingleator class is in gingleator.py <br>
Run for each possible threshold 100 times, totally 1000 times of running short burst. <br>
The step is 10, and length is 10.<br>
Always find the maximum Majority Minority(Black in Louisiana). <br>
