# Springboard_Capstone2

## What Makes a Valuable or Fake Customer Review?
*Currently a work-in-progress*

### The Problem
Business owners often do not have the time to read through every customer review, especially when there are thousands of them. The problem with large amounts of customer reviews is that they can be repetitive, and sometimes they are computer generated. Customer reviews are nonetheless vital because they can provide valuable feedback on which the business can use to improve products and services. 

Natural Language Processing (NLP) can help businesses to sort and find the informative customer reviews with ease and save a tremendous amount of time. By sifting through the reviews more efficiently, businesses would be able to save time by ignoring the fake reviews, and understand what their customers are truly thinking and feeling. Finding which reviews are similar with a recurring theme (valuable) will provide insight and actionable goals. The aim of this capstone is to explore how NLP can be used to determine which attributes of a review make it valuable or suspicious.

### The Data
Amazon has an open dataset of over 130 million customer reviews collected between 1995 and 2015, available as URL’s at https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt. Each line in the dataset represents one product review. Reviews are grouped by product categories such as apparel, automotive, books, e-books, etc. The columns in the dataset include: ‘marketplace’ (country code), ‘customer_id’, ‘review_id’, ‘product_id’, ‘product_parent’ (random identifier for aggregate reviews for the same product), ‘product_title’, ‘product_category’, ‘star_rating’, ‘helpful_votes’, ‘total_votes’, ‘vine’, ‘verified_purchase’, ‘review_headline’, ‘review_body’, ‘review_date’. 
Complete an exploratory data analysis to answer the following questions:

<ol>
  <li> What is the mean and median number of reviews per customer? </li>
<li> What do the reviews of a highly active (>500 reviews) reviewer look like? </li>
<li> What do the reviews that a one review customer look like? </li>
<li> Do customers who write different amounts of reviews give the same distribution of star ratings? </li>
  </ol>
