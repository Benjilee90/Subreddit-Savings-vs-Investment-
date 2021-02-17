# Subreddit Classification
---

## Introduction

Reddit is an American social news aggregation, web content rating, and discussion website. Registered members submit content to the site such as links, text posts, and images, which are then voted up or down by other members. Posts are organized by subject into user-created boards called "subreddits", which cover a variety of topics such as news, politics, science, movies, video games, music, books, sports, fitness, cooking, pets, and image-sharing. Submissions with more up-votes appear towards the top of their subreddit and, if they receive enough up-votes, ultimately on the site's front page. Despite strict rules prohibiting harassment, Reddit's administrators spend considerable resources on moderating the site.

In this study two subreddit were examined; (1) r/SavingMoney and (2) r/Investing. Both topics revolves around the idea of preparing for the future with the emphasis of money. However, while being similar in nature where money is the center of gravity, the ultilization of it is different in concept as one emphasize the importance of saving while another shares the idea of growing wealth through investment. The goal of this project is therefore to try and figure out how distinct these concepts are from one to another. 

## Problem Statement

We, a consultation firm (Data Insights Pte Ltd), was recently **engaged by ABC bank** to predict whether if a particular post within a given subreddit is savings related as the bank wants to better engage their customers on savings based on ground sentiments. A classification model will be devised and evaluated based on accuracy score.

## Conculsion

In general, both subreddit(r/investing & r/SavingMoney) are quite distinct from one another as the average accuracy of the model ranges from 50 to 90% with the highest being 95%. While both revolves around money, the way in which how the money is ultilized is different. Hence, the correlated words used in the prediction is not highly correlated between post as shown in the EDA process. 

During the model selection, the Naive Bayes and TdifVectorizer model is able predict with an accuracy of 95% based on the testing data and 98.6% based on the training. Among all the features, between title, post and combining both, post seems to give the best results in terms of accuracy and computing time. While combing both title and post may increase the accruary, it is limited with the max number of features allowed to pass through the model and requires longer computing time. Among all the model, it proves to be the best as it is not overfitted and has the highest accuracy for test data when indentifying saving related post as tasked by our cilent.<br>

However, the model has some limitation. Currently, there are some misclassfied words within the model which will throw the prediction off if the words appears within a post that may not be savings related. The words should be removed to increase the accuracy of the model.

## Data Dictionary

|S/N|Feature|Data Type|Dataset|Description|
|---|---|---|---|---|
|1|**subreddit**|*int*|combine|Mapped as 1 for SavingMoney, 0 for Investment| 
|2|**id**|*str*|combine|The identification of the person who posted the post|
|3|**title**|*str*|combine|The title of the subreddit post|
|4|**selftext**|*str*|combine|The body of the post|
|5|**title_len**|*flaot*|combine|The length of the title|
|6|**text_len**|*float*|combine|The length of the body|
|7|**title_cleaned**|*str*|combine|The processed title|
|8|**selftext_cleaned**|*str*|combine|The processed body of post|
|9|**titlepost**|*str*|combine|The combination of processed title and post|