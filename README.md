# Springboard Data Science Capstone 2
In this project, I created a machine learning model that leverages Natural Language Processing (NLP) and the behavior of reviewers to automatically classify fraudulent reviews. By sifting through the reviews more efficiently, a machine learning model can help platforms like Amazon maintain high standards of quality in their marketplace. In this project labels were created to allow for supervised training of Random Forest, Multinomial Naive Bayes and Linear SVC models. 

## Detecting Fake Amazon Reviews With Machine Learning

Important files to view:
<li> <a href='https://github.com/chantel808/Springboard_Capstone2/blob/master/Capstone%202%20Final%20Report%20-%20CClark.pdf'> Final Report </a></li>
<li> <a href='https://github.com/chantel808/Springboard_Capstone2/blob/master/Amazon_reviews_NLP_CClark.ipynb'> NLP Python notebook </a> </li>
<li> <a href='https://github.com/chantel808/Springboard_Capstone2/blob/master/Amazon_reviews_EDA_CClark.ipynb'> Exploratory Data Analysis Python notebook </a> </li>
<li> <a href='https://github.com/chantel808/Springboard_Capstone2/blob/master/Amazon_reviews_stats_CClark.ipynb'> Statistical Analysis </a> </li>
<li> <a href='https://github.com/chantel808/Springboard_Capstone2/blob/master/Capstone2-slide-deck-cclark.pdf'> Slide Deck </a> </li>

### The Problem
A firms’ online reputation is paramount to gaining the trust of potential customers. One way that customers  determine whether or not to buy a product or service is through reading online  reviews. However, it can be difficult to know which of these reviews are authentic. Products with a 5-star review may not actually have a true 5-star rating because of incentivized or paid reviews. This inflation makes it very difficult for firm’s to have their products show up in user searches when another product has over a thousand fake, glowing reviews. Another type of fake review are those that are malicious and aim to destroy the online reputation of competitors. Those can be especially damaging to businesses, because according to a survey by Reviewtrackers, people are less inclined to buy a product if it has less than a 4 out of 5 star rating, and have been deterred from buying products due to a bad review.

Since 2015, Amazon has been working to crack down on the users who write paid reviews as well as companies that solicit them (<a href='https://www.washingtonpost.com/business/economy/how-merchants-secretly-use-facebook-to-flood-amazon-with-fake-reviews/2018/04/23/5dad1e30-4392-11e8-8569-26fda6b404c7_story.html'> Dwoskin and Timberg, 2018 </a>). However, in 2019 <a href='https://reviewmeta.com/'> ReviewMeta </a> found that even products which receive Amazon choice badges contain many suspicious reviews.  Fake reviews pose a problem for both businesses and potential customers. How can companies compete with those that use paid reviews, and how can customers get a true estimate of the quality of product or service?

### The Data
Data was obtained from an open Amazon dataset with over 130 million customer reviews collected between 1995 and 2015. It is available as TSV files on an Amazon Web Services S3 bucket: https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt. Reviews are grouped by product categories, and the apparel dataset with over 5.8 million reviews was used for this project. Each line in the dataset represents one product review. The columns in the dataset used for this project include: 

<li> customer ID - random identifier of author </li>
<li> review ID - unique ID of review  </li>
<li>star rating - ordinal data ranging between 1 and 5 </li>
<li>helpful votes - number of times a review was voted as ‘helpful’ </li>
<li>vine -  a categorical value for whether or not a review was written by an Amazon vine member; vine is an invite-only program, which the most trusted reviewers are invited to </li>
<li>verified purchase - whether or not product was purchased on Amazon </li>
<li>review body - text of the review </li>
<li>review date - date review written </li>

### Summary
Target labels were created based off of the maximum number of reviews written within a day. If a customer wrote 30 or more reviews within a day, all reviews written by the customer were given a target label value of 1 under a 'suspect' column. The image below is a TSNE (t-distributed stochastic neighbor embedding) projection of the TF-IDF vectors from non-suspicious (blue, label ‘0’) and suspicious (green, label ‘1’) reviews in the training set.

<img src="https://github.com/chantel808/Springboard_Capstone2/blob/master/tsne.png">

Cosine similarity of reviews from a 'suspicious' customer:

<img src="https://github.com/chantel808/Springboard_Capstone2/blob/master/cosine_similarity.png" width="500" height="500">

Frequency of posts from a highly 'suspicious' customer:

<img src="https://github.com/chantel808/Springboard_Capstone2/blob/master/suspect_revs_per_day.png" width="400" height="250">

Vine vs. 'suspicious' total reviews per customer:

<img src="https://github.com/chantel808/Springboard_Capstone2/blob/master/vine_total_revs.png" width="400">

Features included the review body, star rating, number of helpful votes, vine, verified purchase, and the author's average cosine similary of the most similar reviews. A FeatureUnion pipeline was used to transform and combine the different types of features.

![Feature pipeline](https://github.com/chantel808/Springboard_Capstone2/blob/master/feature_pipeline_rs.png)

The machine learning algorithms tested included Multinomial Naive Bayes, Random Forests, and Linear SVC.

<!-- <img src="" width="400" height="400"> -->
