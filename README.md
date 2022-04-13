# amazon_reviews_proj

<b>Background</b>

The objective of this project was to understand what makes a customer review helpful on eCommerce websites such as Amazon.com.

COVID-19 pandemic has caused a massive shift in consumer behavior and an extraordinary surge in the eCommerce industry. The volume of transactions on online marketplaces continue to grow as customers have turned to online shopping more than ever before.

Due to this shift, customer reviews on eCommerce websites have significantly increased over the last few years.
Based on a survey conducted in the US on on customer attitudes towards online shopping in 2021, 48% of the participants indicated that they find customer reviews on the internet very helpful. Customer reviews can therefore play an important role in influencing purchase decision of users.

![](/images/attitudes-towards-online-shopping-in-the-us-2021.png)

In this project, I worked with a dataset of around 3 million reviews from Amazon.com across three different product categories to analyze the reviews text data and determine how a review's extremity, length, or sentiment affect its perceived helpfulness. 

<b> Process and Initial Findings </b>

EDA was performed on the full dataset to understand what factors contribute to helpfulness of reviews. First finding was that while the fraction of verified reviews since 2008 increased by 58%, the helpfulness of the reviews decreased significantly by 50% in these 10 years.

![](/images/helpful_verified_reviews_vs_time.JPG)

First factor that was considered was how number of reviews and word count per review has changed over the years. Home and kitchen products started making up more than 50% of the total reviews since 2010 while book reviews have recently only been a small fraction of the total reviews. 

![](/images/number_of_reviews_by_product_type_vs_year.JPG)

Another interesting pattern that was observed is that the word count per review dropped by 78% since 2010 which may be due to a smaller fraction of book reviews. This observation supports the hypothesis that lengthier reviews tend to be more helpful, and they are written mostly by book readers.

![](/images/word_count_per_review_vs_year.JPG)

<b>Does helpfulness of reviews change by product type?</b> 
I decided to categorize the products into two types – search products, that tend to be easy to evaluate before buying such as home and kitchen products, and experience products such as video games that are often assessed only after a user has interacted with the product. An interesting finding was that a greater fraction of extreme reviews (or reviews with a rating of 1 or 5) tend to be comparatively more helpful for search products.

![](/images/home_kitchen_helpful_reviews_word_count.JPG)

Lengthier reviews tend to be more helpful for experience products as the word count distribution appeared to be more right-skewed for home and kitchen reviews, but for video games it seemed a bit more balanced. This makes sense since experience products are typically more difficult to assess before buying, so a long, detailed review can add more value for other buyers. 

![](/images/video_games_helpful_reviews_word_count.JPG)

<b> Comparing helpful vs non-helpful reviewers</b>
Word clouds were used to compare the usage of words by two different users – one with a strong history of writing helpful reviews and other whose past reviews have usually been unhelpful. A clear difference was found as the words used by the helpful reviewer were descriptive, included relevant product details, while the non-helpful reviewer used a lot of adjectives and subjective words. In the word cloud for helpful reviews below, usage of words such as book, war, author, work, friend, history, etc. was more common compared to non-helpful reviews.

![](/images/word_cloud_helpful.JPG)

<b> Topic Modelling and POS Frequency </b>

Here I found a clear difference in variety of words used by the two different reviewers. The teal-colored bar represents frequency of tokens in all the reviews, while dark blue bar represents what fraction of the topic is made up by a given token. The left visual has a rich variety of descriptive words compared to repetition in the non-helpful review as only a few words make up the topic on the right. 

![](/images/topic_modeling_both.JPG)

While performing Part of Speech (POS) tag frequencies analysis, I found that 75% of the top 10,000 most frequently used words in helpful reviews were nouns which in comparison to non-helpful reviews was higher. This further supports the observation that helpful reviews are more descriptive in nature, and have a much greater depth.

![](/images/POS_frequency_top_words_in_helpful_reviews.JPG)


<b> Usage of images and video links in reviews </b>

When review text contained image or video links, a much greater fraction of the reviews tend to be helpful. About 51% of the almost 20,000 reviews that contained a hyperlink were helpful, and this increased to 71% for reviews that contained video links even though they were a much smaller fraction. 

![](/images/images_videos_relation_with_helpfulness.JPG)

<b> Sentiment Analysis </b>

Next, I analyzed how sentiments and rating given to a product are related to helpfulness of a review.

-	The average compound sentiment scores increased significantly in the last few years as the reviews became more positive, but the helpfulness of the reviews keeps dropping. Years 2005 and 2013 are shown for comparison and the sentiment score increased by 0.15 in this duration, but helpfulness dropped by 60%.
-	44% of the helpful reviews received a rating of 1 compared to only 14% for five-star reviews. 
-	This shows that only part of my hypothesis was correct, since users tend to put a lot more helpful detail when writing reviews after having a negative experience, and only generic subjective text when they have had a strong positive experience which doesn’t help much.


![](/images/sentiment_scores_vs_year.JPG)

![](/images/helpful_reviews_vs_ratings.JPG)

<b> Conclusion </b>

The table below summarizes some of the key findings of the EDA in this project. Helpful reviews tend to be lengthier and have an average word count of 183 words, lower average overall rating of 3.85 compared to 4.42 for non-helpful reviews, and a higher neutral sentiment score. Another aspect that makes a review helpful is the use of objective instead of abstract words to describe the experience in detail and using visuals or reference links. Year 2006 had the highest fraction of helpful reviews, and book reviews made up 63% of the total reviews in this year which dropped a lot by 2018. 

![](/images/summary_conclusion_helpful_vs_not_helpful.JPG)

