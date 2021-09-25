# NCAAW-competition (Top 7%)
https://www.kaggle.com/c/ncaaw-march-mania-2021

## Competition Overview

Based on historical data of NCAA games, the goal of the competition was to predict winner and losers of the women's NCAA basketball tournament. 

I am not a huge fan of basketball, even I never watch it. But, I wanted to improve my skills at acquiring domain knowledge. I thought that this competition would be perfect for that because it seemed that feature engineering would play a huge part. In this competition, I did not build fancy models (I used a simple XGBoost model). For me the goal was to develop in a short time a good understanding of basketball in order to perform a deep feature engineering.

I started by reading a lot of blogs of basketball enthusiasts, then I tried to understand KenPom features. Based on the domain knowledge that I acquired, I created new features (see the notebook) and I created a KenPom Scraper to extract KenPom features. This is where I discovered that KenPom features where leaking because they were updated even after the end of the tournaments. At the end, I did not use the scraper since the data was leaking.

I decided to focus on the NCAAW Competition instead of the NCAAM because after looking at the previous competitions, I saw that a lot of people where manipulating the predictions of their models based on their beliefs in the NCAAM competition. It was less the case in the NCAAW competition since less people look at women's basketball.

# Tabular Playground Series February (Top 2%)

## Competition Overview

In January 2021, Kaggle had the amazing idea of creating month-long tabular playground to train our tabular data skillsets. The dataset used for this competition is synthetic, but based on real data and generated using CTGAN. 

Why did I participate in this competition ?

I knew that during my internships, I will have to work with gradient boosting algorithms. Therefore, I wanted to deep dive into the training of these models. During this competition, I learned how to tune their hyperparameters using Optuna and I also discovered a new way of training them to slightly improve their performance.

How it works ?

* Train your best model
* Decrease learning rate and train the model again
* Decrease regularization params and retrain the model

Explanations

This strategy is mostly based on transfer learning (mostly used in neural networks). In transfer learning, we use a pretrained model and add a head to it. Moreover, we usually froze lower layers (the ones of the pretrained model) and train higher layers (those that we add to the pretrained model). This is exactly the case here:

We create a normal lgbm model and fit it on our data. Once it starts overfitting we stop the training. We will consider this part of the lgbm model as the pretrained model (to make an analogy to neural networks).

After that, and in order to fight against overfitting, we decrease learning rate and starts fitting again the pretrained model on our data, in other words we add more weak learners to our lgbm model (that can be compared to higher layers in a neural network). We can also make an analogy to neural networks in this case. Indeed, when we train neural networks, it is good practice to decrease the learning rate during training process.

Once reducing the learning rate is not adding a significant improvement to our model, we should increase the complexity of our weak learners. Indeed, increasing weak learners complexity might increase their performance while also increasing their chance of overfitting. At inference time, we will have weak learners with high bias and low variance (weak learners from the pretrained model) and some which are slightly overfit (low bias- high variance). This is why we reduce the learning rate before adding overfitted weak learners (when we reduce learning rate, we basically reduce the contribution of these overfitted trees to final prediction).

I tried many things in order to increase model compelxity and decrease regularization params. I found that the best thing to do is to increase number of leaves and decrease minimum child samples.

# Riiid Answer Correctness (Top 9%)

## Competition Overview



