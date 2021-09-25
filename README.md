# NCAAW-competition
https://www.kaggle.com/c/ncaaw-march-mania-2021

## Competition Overview

Based on historical data of NCAA games, the goal of the competition was to predict winner and losers of the women's NCAA basketball tournament. 

I am not a huge fan of basketball, even I never watch it. But, I wanted to improve my skills at acquiring domain knowledge. I thought that this competition would be perfect for that because it seemed that feature engineering would play a huge part. In this competition, I did not build fancy models (I used a simple XGBoost model). For me the goal was to develop in a short time a good understanding of basketball in order to perform a deep feature engineering.

I started by reading a lot of blogs of basketball enthusiasts, then I tried to understand KenPom features. Based on the domain knowledge that I acquired, I created new features (see the notebook) and I created a KenPom Scraper to extract KenPom features. This is where I discovered that KenPom features where leaking because they were updated even after the end of the tournaments. At the end, I did not use the scraper since the data was leaking.

I decided to focus on the NCAAW Competition instead of the NCAAM because after looking at the previous competitions, I saw that a lot of people where manipulating the predictions of their models based on their beliefs in the NCAAM competition. It was less the case in the NCAAW competition since less people look at women's basketball.

# Tabular Playground Series February

## Competition Overview


# Riiid Answer Correctness

## Competition Overview



