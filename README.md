# amazon_reviews_proj

<b>Background</b>

The objective of this project was to understand what makes a customer review helpful on ecommerce websites such as Amazon.com.

COVID-19 pandemic has caused a massive shift in consumer behavior and an extraordinary surge in the eCommerce industry. The volume of transactions on online marketplaces continue to grow as customers have turned to online shopping more than ever before.

Due to this shift, customer reviews on eCommerce websites have significantly increased over the last few years.
Based on a survey conducted in the US on on customer attitudes towards online shopping in 2021, 48% of the participants indicated that they find customer reviews on the internet very helpful. Customer reviews can therefore play an important role in influencing purchase decision of users.

![](/images/attitudes-towards-online-shopping-in-the-us-2021.png)

In this project, I worked with a dataset of around 3 million reviews from Amazon.com across three different product categories to analyze the reviews text data and determine how a review's extremity, length, or sentiment affect its perceived helpfulness. 

<b> Process and Initial Findings </b>

EDA was performed on the full dataset to understand what factors contribute to helpfulness of reviews. First finding was that while the fraction of verified reviews since 2008 increased by 58%, the helpfulness of the reviews decreased significantly by 50% in these 10 years.

![](/images/attitudes-towards-online-shopping-in-the-us-2021.png)

-	First factor that was considered was how number of reviews and word count per review has changed over the years.
-	Home and kitchen products started making up more than 50% of the total reviews since 2010 while book reviews have recently only been a small fraction of the total reviews. 
-	Another interesting pattern that was observed is that the word count per review dropped by 78% since 2010 which may be due to a smaller fraction of book reviews.
-	This observation supports the hypothesis that lengthier reviews tend to be more helpful, and they are written mostly by book readers.


<b>Does helpfulness of reviews change by product type?</b> 
-	I decided to categorize the products into two types – search products, that tend to be easy to evaluate before buying such as home and kitchen products, and experience products such as video games that are often assessed only after a user has interacted with the product.
-	An interesting finding was that a greater fraction of extreme reviews (or reviews with a rating of 1 or 5) tend to be comparatively more helpful for search products.
-	Lengthier reviews tend to be more helpful for experience products as the word count distribution appeared to be more right-skewed for home and kitchen reviews, but for video games it seemed a bit more balanced. 
-	This makes sense since experience products are typically more difficult to assess before buying, so a long, detailed review can add more value for other buyers. 

<b> Comparing helpful vs non-helpful reviewers</b>
-	Word clouds were used to compare the usage of words by two different users – one with a strong history of writing helpful reviews and other whose past reviews have usually been unhelpful.
-	A clear difference was found as the words used by the helpful reviewer were descriptive, included relevant product details, while the non-helpful reviewer used a lot of adjectives and subjective words. 


