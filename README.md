# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)  Project 3: Web APIs & Classification

### Contents:
- [Background](#Background)
- [Problem Statement](#Problem-Statement)
- [Summary of Analysis](#Summary-of-Analysis)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

# Background

Microsoft Surface is a series of touch-screen mobile laptop which is renowned for combining tablet and laptop seamlessly. Apple iPad is always the go-to tablet which beat competitor like Samsung Galaxy Tab and has the most sale in the past decade. However, many companies have launch tablet-like product lines and took away marketshare from apple's product. Apple ,then, launch iPad Pro and magic keyboard which make it can also works as a working laptop.

<p align="center">
<img src="../images/best_selling_tablets.PNG" width="800" />
</p>

[*source: https://www.statista.com/statistics/276635/market-share-held-by-tablet-vendors/*](https://www.statista.com/statistics/276635/market-share-held-by-tablet-vendors/)

While iPad is the better tablet, and it’s ideal for creative tasks, Surface is always a better laptop, well suited for tasks like writing, editing large spreadsheets and databases, and programming. With the coming of iPad with better keyboard, Microsoft has to come-up with a new idea or set next standard to prevent apple taking away the revenue is this competitive hardware market.

<p align="center">
<img src="../images/surface_vs_ipad.jpg" width="400" />
</p>

Reddit is a network of communities based on people's interests. It is the massive places that people came to talk about specific topic whether to share a story ,asking question, or leaving a negative comments. Going through Reddit can tell you the trends of thing happening in that topic. Suppose that Microsoft want to develop its Surface series, as a Product Manager, the model that be able to classify post from subreddit of surface and ipad is created based on its title and context  and further analyzed to find keywords and hoping to see a diffent key interest of people in both communities.


# Problem Statement

What is the keyword most appear in surface and ipad subreddit post? Are they the negative or positive words? And how to make a development of surface series based on surface's weakness or ipad's strength?


# Summary of Analysis

The model used to classify posts from surface and ipad subreddit is a combination of CountVectorizer and LogisticRegression.Countvectorizer chop the text or sentence into words while logisticregression use regression model to predict whether the following sets of word come from which subreddit.

Final model has accuracy of 84% on testing datasets. When the wrong predictions are studied, it was found that if the post contains a strong correlate word to each brand such as 'window' (surface-leaning side) or 'app' (ipad-leaning side), the model is likely to predict incorrectly,whichcan be improved by adding stopword/words used to remove from texts used for training model.

When looking at feature importance or how the words impact the prediction of the model,the model showed that the words like
- apple,ios,magic,pencil,safari

show a strong correlation for ipad topics because this set of words is apple's renowned product. This indicates that apple has a strong marketing campaign and product characteristics.

While, for surface subreddit, top keywords for model predicting this class are

- book,sp (surface pro),pen,microsoft,sb (surface book)

which are also a identity of microsoft surface line up. But also negative words have came up such as

- fix,replace

This indicated that microsoft surface still has some flaws. If the company has the ability to reduce the number of warranty claims or repairing claims. It should be able to increase products' brand , revenue and marketshare. Also apart from the model line-up, if microsoft can launch accessories or any aesthetic items, it should be able to attract new customers from apple side as well

# Conclusions and Recommendations

Based on our problem statement, we found that
1. Keywords that make model predict ipad are Apple's product which is well known such as ios,magic keyboard or apple pencil and the model didn't show much of negative words in those keyword.
2. While surfaces' keyword also showed the same trend except that there are negative words like 'fix' or 'replace'

To make a surface product better, it is recommended that
1. Microsoft should consider improving product endurance to reduce number of warranty claim.
2. Microsoft should consider launching aesthetic products/items for surface line-ups