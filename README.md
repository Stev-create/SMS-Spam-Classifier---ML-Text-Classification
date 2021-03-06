<h1> SMS-Spam-Classifier---ML_Classification </h1>

## Context

This dataset taken from [UCI](https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection). 

<p>http://www.dt.fee.unicamp.br/~tiago/smsspamcollection/</p>

## Overview

In this Project, I use Machine Learning Approach to classify SMS Messages in Spam or in Ham. Where <b>Multinominal Naive Bayes and XGBoost Classifier Model</b> has been used in this Project. And the Best Model Based on Precision. A summary results can be seen below, but for details can be seen in [this notebook](https://github.com/Stev-create/SMS-Spam-Classifier---ML-Text-Classification/blob/master/SMS%20Spam%20Classifier.ipynb).

## Summary

### Exploratory Data Analysis

In exploration, we should know how our model will classify Spam Messages and Ham Messages. As we can see below, spam messages tend to have longer length than ham messages. And I think, its make sense, spam messages usually is about 'fake' winning lottery messages or fake messages that are considered important. At the same time, ham messages is usualy an instant messages with many slang abbreviation. 

![GitHub Logo](/images/c.png)

![GitHub Logo](/images/d.png)


## Statistical Analysis

After that, I want to know is it significance? So I perform Normality Test using Shapiro-Wilk Test and Significance Test using Mann-Whitney U Test. The results of Mann-Whitney U Test can be seen below.

|   | Hypothesis | 
| :---: | :---: |
| length  | Reject Null Hypothesis  | 
| words | Reject Null Hypothesis | 

### Words Cloud

At last, I want to know, what words are often appear in ham or spam messages. So I need to visualize it, using WordCloud. The Word Cloud of Spam Messages:

![GitHub Logo](/images/3.png)

As expected, words that many often in the spam messages is <i>free, have won, text, please call, </i> and <i> reply </i>. Like the one who get the messages win lottery or something and feel like an invitation to do something. And Word Cloud of Ham Messages:

![GitHub Logo](/images/4.png)

Well, its same as we expected right? Many slang abbreviation.


### Evaluation Metrics

This dataset can be considered as a highly imbalanced. So we need to careful to pick what evaluation metric we'll use. And i want my model have low False Positive numbers. That's why my objective is to have a model with high precision score.

| Classifier  | precision (pos label = 1)| precision (pos label = 0) |
| :---: | :---: | :--: |
| Multinominal Naive Bayes  | 0.98  | 0.98 |
| XGBoost Classifier  | 0.92  | 0.97 |

label = 1 --> spam <br> 
label = 0 --> ham

if we look again in EDA Part, it is not surprising to see both models working so well in classify the spam messages and ham messages. Even without a model, just use a simple visualization, we can predict where the spam messages and where the ham messages. So, the Multinominal Naive Bayes work better than XGBoost. To see the sanity check, check out [this notebook](https://github.com/Stev-create/SMS-Spam-Classifier---ML-Text-Classification/blob/master/SMS%20Spam%20Classifier.ipynb).

# Thank you






