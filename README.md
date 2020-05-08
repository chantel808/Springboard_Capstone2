# Springboard Capstone2

## What Makes a Valuable or Fake Customer Review?
*Currently a work-in-progress*

Important files to view:
<li> <a href='https://github.com/chantel808/Springboard_Capstone2/blob/master/Capstone%202%20Milestone%20Report%202%20-%20CClark.pdf'> Milestone Report 2 </a></li>
<li> <a href='https://github.com/chantel808/Springboard_Capstone2/blob/master/Amazon_reviews_NLP_CClark-Copy3.ipynb'> NLP Python notebook </a> </li>
<li> <a href='https://github.com/chantel808/Springboard_Capstone2/blob/master/Amazon_reviews_EDA_CClark.ipynb'> Exploratory Data Analysis Python notebook </a> </li>
<li> <a href='https://github.com/chantel808/Springboard_Capstone2/blob/master/Amazon_reviews_stats_CClark.ipynb'> Statistical Analysis </a> </li>

### The Problem
The online reputation of businesses is extremely important these days in gaining the trust of customers. One way that people determine whether or not to buy a product or service is through reading customer reviews. However, it can be difficult to know which reviews are authentic because of the presence of ‘fake’ reviews. Products on Amazon with a 5-star review may not actually have a true 5-star rating because of a flood of incentivized or paid reviews. The inflation of reviews makes it very difficult for the average or ethical company to have their products show up in user searches when another product has over a thousand fake, glowing reviews. Since 2015, Amazon has been working to crack down on the users who write paid reviews, and companies that solicit them (<a href='https://www.washingtonpost.com/business/economy/how-merchants-secretly-use-facebook-to-flood-amazon-with-fake-reviews/2018/04/23/5dad1e30-4392-11e8-8569-26fda6b404c7_story.html'> Dwoskin and Timberg, 2018 </a>). However, in 2019 <a href='https://reviewmeta.com/'> ReviewMeta </a> found that even products which receive Amazon choice badges contain many suspicious reviews.  Fake reviews pose a problem for both businesses and potential customers. How can companies compete with those that use paid reviews, and how can customers get a true estimate of the quality of product or service?

A machine learning model that uses Natural Language Processing (NLP) and reviewer metrics can help customers to obtain the true quality of online products by removing suspicious reviews and finding the valuable and unique reviews. By sifting through the reviews more efficiently, a machine learning model can help customers to save time and money when shopping online. The aim of this capstone is to explore how NLP can be used in combination with reviewer metrics to determine what makes a review valuable or suspicious.


### The Data
Amazon has an open dataset of over 130 million customer reviews collected between 1995 and 2015, available as URL’s at https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt. Each line in the dataset represents one product review. Reviews are grouped by product categories such as apparel, automotive, books, e-books, etc. The columns in the dataset include: ‘marketplace’ (country code), ‘customer_id’, ‘review_id’, ‘product_id’, ‘product_parent’ (random identifier for aggregate reviews for the same product), ‘product_title’, ‘product_category’, ‘star_rating’, ‘helpful_votes’, ‘total_votes’, ‘vine’, ‘verified_purchase’, ‘review_headline’, ‘review_body’, ‘review_date’. 
Complete an exploratory data analysis to answer the following questions:

<ol>
  <li> What is the mean and median number of reviews per customer? </li>
<li> What do the reviews of a highly active (>500 reviews) reviewer look like? </li>
<li> What do the reviews that a one review customer look like? </li>
<li> Do customers who write different amounts of reviews give the same distribution of star ratings? </li>
  </ol>
