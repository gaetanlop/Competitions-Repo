# NCAAW-competition
https://www.kaggle.com/c/ncaaw-march-mania-2021

## Competition Overview

Based on historical data of NCAA games, the goal of the competition was to predict winner and losers of the women's NCAA basketball tournament. I am not a huge fan of basketball, even I never watch basketball. But, I wanted to improve my skills at acquiring domain knowledge. I thought that this competition would be perfect for that because it seemed that feature engineering would play a huge part. In this competition, I did not build fancy models (I used a simple XGBoost model). For me the goal was to develop in a short time a good understanding of basketball in order to perform a deep feature engineering.

I started by reading a lot of blogs of basketball enthusiasts, then I tried to understand KenPom features. Based on the domain knowledge that I acquired, I created new features (see the notebook) and I created a KenPom Scraper to extract KenPom features. This is where I discovered that KenPom features where leaking because they were updated even after the end of the tournaments.

I decided to focus on the NCAAW Competition instead of the NCAAM because after looking at the previous competitions, I saw that a lot of people where manipulating the predictions of their models based on their beliefs in the NCAAM competition. It was less the case in the NCAAW competition since less people look at women's basketball.


* 03/03 : started feature engineering on 2 datatsets: season compact, seed 
* 04/03 : finished feature engineering -> Simple training set created
* 07/03 : built an inference pipeline and make one baseline submission (baseline is broken)
* 08/03 : reworked my baseline and make it work. Made one submission. Add rank feature.
* 09/03 : implemented features of this website: https://thepowerrank.com/cbb-analytics/
* 10/03 : built a KenPom scrapper from scratch using bs. Also created feature offensive efficiency
* 11/03 : build NCAAW pipeline + tried another way to increase the number of data points + hyperparameter tuning
* 13/03 : NCAAW hyperparameter tuning
* 14/03 : NCAAW worked on feature selection, made the pipeline for 2021 predictions
* 15/03 : Everything ready for woman
* 16/03 : Everything ready for man. Just one notebook style in hyperparameter tuning. I scrapoped Kenpom data without leakage from 2011 to 2021.
* 17/03 : Add another column to kenpom data: adj_em. It seems that it is the most important features. I also maid my conservative submission. I am crezting my aggressive submission mostly based on kenpom data
* 18/03 : Create Spread notebook and tuned hyperparameters with optuna
* 19/03 : Submit Spread for men competition + prepared spread for women competition. I also submitted women competition
* 20/03 : Submit women spread competition

## Path to top 7%
I need to talk about the path to the top 7% and also the competition overview. What where we asked for and everything.

# Tabular Playground Series February

## Competition Overview


# Riiid Answer Correctness

## Competition Overview



