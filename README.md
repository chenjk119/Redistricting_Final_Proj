# Redistricting_Final_Proj

## Table of Contents
- [Data](#data)
- [Outlier Analysis](#outlier-analysis)
- [Signature of Gerrymandering](#signature-of-gerrymandering)
- [Short Burst](#short-burst)

## Data
[LA_MAUP.ipynb](LA_MAUP.ipynb) <br>
The data are retrieved from Redistricting Data Hub on 04/10/2024.

All data used in this project:
- [Louisiana block PL 94-171 2020 (by table)](https://redistrictingdatahub.org/dataset/louisiana-block-pl-94171-2020-by-table/)
- [VEST 2020 Louisiana precinct and election results](https://redistrictingdatahub.org/dataset/vest-2020-louisiana-precinct-and-election-results/)
- [2022 Louisiana Congressional Districts Approved Plan](https://redistrictingdatahub.org/dataset/2022-louisiana-congressional-districts-approved-plan/)

The data are cleaned up and fixed using maup.smart_repair(), the maup.doctor() returns true.

## Outlier Analysis
[Metrics.ipynb](Metrics.ipynb)

[Cut_edges.ipynb](Cut_edges.ipynb)

These two files includes a Markov Chain, and functions to calculate Efficiency gap, Mean-median difference, Dem-won districts and cut edges for both elections. 
The results are plotted as histogram:
- [Efficiency Gap 2020 President Election](images/efficiency_gap_for_president.png)
- [Efficiency Gap 2020 Senate Election](images/eff_gap_senate.png)
- [Mean-median Difference 2020 President Election](images/mean_median_diff_for_2020_president.png)
- [Mean-median Difference 2020 Senate Election](images/mean_median_diff_senate.png)
- [Dem-won Districts 2020 President Election](images/won_by_demo_president.png)
- [Dem-won Districts 2020 Senate Election](images/won_by_demo_senate.png)
- [Cut Edges](images/cut_edges.png)

## Signature of Gerrymandering
[Signature_of_Gerrymandering.ipynb](Signature_of_Gerrymandering.ipynb)

This file includes a Markov Chain, results of signature of gerrymandering in form of marginal box plots for both elections.
- [2020 President](images/box1.png)
- [2020 Senate](images/box2.png)

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
