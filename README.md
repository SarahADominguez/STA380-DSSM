---
editor_options: 
  markdown: 
    wrap: 72
---

# README

## Table of Contents

1.  [Introduction](#1-introduction)
2.  [Questions](#2-questions)
3.  [Overview](#3-overview)
    -   [Probability practice](#probability-practice)
    -   [Wrangling the Billboard Top
        100](#wrangling-the-billboard-top-100)
    -   [Visual story telling part 1: green
        buildings](#visual-story-telling-part-1-green-buildings)
    -   [Visual story telling part 2: Capital Metro
        data](#visual-story-telling-part-2-capital-metro-data)
    -   [Clustering and dimensionality
        reduction](#clustering-and-dimensionality-reduction)
    -   [Market segmentation](#market-segmentation)
    -   [The Reuters Corpus](#the-reuters-corpus)
    -   [Association rule mining](#association-rule-mining)
    -   [Image classification with neural
        networks](#image-classification-with-neural-networks)
4.  [Installation/Requirements](#4-installationrequirements)
5.  [File Descriptions](#5-file-descriptions)
6.  [Contributors/Team](#6-contributorsteam)

***\*Disclaimer:** There are multiple files for some of the problems
because we as a team could not collectively figure out how to add in our
pictures and graphs in only one .md file due to lack of github
expertise, so several problems have graphs/insights uploaded separately
or have .pdf files as well to show pictures and code.*

## 1. Introduction

For our “Introduction to Machine Learning” assignment, our team has
conducted an in-depth exploration of key ML concepts. Our work covers
the core principles of probability, advanced data wrangling techniques,
the craft of visual storytelling, methodologies in clustering and topic
modeling, and the complexities of neural networks. We encourage you to
explore our repository for a thorough analysis and valuable insights.

## 2. Questions

-   **Q1. Probability practice** (ML—Probability.md)
-   **Q2. Wrangling the Billboard Top 100**
    (ML—Data-Wrangling-Billboard.md/ML—Data-Wrangling-Billboard.pdf)
-   **Q3. Visual story telling part 1: green buildings** (ML—Visual
    story telling part 1 green buildings.ipynb)
-   **Q4. Visual story telling part 2: Capital Metro data**
    (ML—Visual-Story-Telling-Part-2—Cap-Metro.md/ML—Visual-Story-Telling-Part-2—Cap-Metro.pdf)
-   **Q5. Clustering and dimensionality reduction**(ML—Clustering and
    dimensionality reduction.ipynb)
-   **Q6. Market segmentation**(ML—Market segmentation.ipynb)
-   **Q7. The Reuters Corpus**(Prob\_(7)*The_Reuters_Corpus*.ipynb)
-   **Q8. Association rule
    mining**(Machine-Learning-Prob-8-Association-Rule-Mining.md)
-   **Q9. Image classification with neural networks**(ML—Image
    Classification With Neural Networks.ipynb)

## 3. Overview

### $$Probability practice$$ {#probability-practice}

**Description:** - In our analysis, we utilized the Rule of Total
Probability to determine the proportion of truthful respondents
answering “yes” in a website survey scenario (Part A). Following this,
we applied Bayes’ Theorem to evaluate the probability of disease
presence given a positive test result, factoring in both the test’s
sensitivity and the prevalence of the disease (Part B).

**Conclusions/Results:** \* The fraction of people who are truthful
clickers answered yes is 71.43%. The probability of someone having
disease given that they tested positive is 19.89%

### $$Wrangling the Billboard Top 100$$ {#wrangling-the-billboard-top-100}

**Description**

The analysis included wrangling and visualizing data from the Billboard
Top 100 chart, covering every song from 1958 through mid-2021. We
focused on three key aspects:

Identifying the top 10 most popular songs based on their presence on the
chart.

Analyzing the musical diversity over time by the number of unique songs
each year.

Finding 19 artists who have had at least 30 songs that were “ten-week
hits.”

**Results**

Top 10 Popular Songs: Songs such as “Radioactive” by Imagine Dragons and
“Blinding Lights” by The Weeknd were identified among the top 10, with
the counts indicating the number of weeks they remained on the chart.

Musical Diversity: A line graph illustrated a peak in diversity in 1966,
followed by a decline until 2001, and then a rise, showing the variation
in unique songs over time.

Artists with Ten-Week Hits: A bar plot showcased artists like Elton John
and Madonna who have had notable ten-week hits, with Elton John topping
the list.

### $$Visual story telling part 1: green buildings$$ {#visual-story-telling-part-1-green-buildings}

**Description**

The project investigates the financial impact of green certification on
commercial rental properties. Specifically, it examines whether green
buildings command higher rents than non-green buildings. The analysis
uses a dataset containing 7,894 commercial rental properties, with 685
of them being green-certified. The main variable of interest is the
median rent per square foot per year, which is compared between
green-certified and non-green buildings.

**Results**

-   **Median Rent for Green Buildings:** \$27.60 per square foot per
    year

-   **Median Rent for Non-Green Buildings:** \$25.00 per square foot per
    year

-   **Rent Premium for Green Buildings:** \$2.60 per square foot per
    year

The results indicate that green-certified buildings command a rent
premium of \$2.60 per square foot per year compared to non-green
buildings.

**Conclusion**

The analysis concludes that there is a positive rent premium associated
with green-certified commercial buildings. This suggests that tenants
are willing to pay more for properties with green certifications, likely
due to benefits such as energy efficiency, sustainability, and possibly
better work environments.

### $$Visual story telling part 2: Capital Metro data$$ {#visual-story-telling-part-2-capital-metro-data}

**Description**

The analysis examines ridership patterns in Austin’s Capital Metro bus
network around the UT-Austin campus, focusing on factors such as peak
hours, differences between weekdays and weekends, the impact of
temperature, seasonal variations, and the relationship between boarding
and alighting.

**Results**

**1.) Average Ridership by Time of Day (Weekdays):** This line graph
shows ridership patterns on weekdays, with distinct morning peaks
between 7 AM and 9 AM and evening peaks from 4 PM to 6 PM. It highlights
that commuter rush hours have the highest ridership, with slight
variations, particularly on Fridays.

**2.) Average Ridership by Time of Day (Weekends):** This graph
illustrates weekend ridership patterns, showing a gradual increase in
the morning and stable levels during midday. Saturday has higher
ridership, especially in the evening, compared to Sunday. Peak ridership
occurs between 4 PM and 6 PM on both days, followed by a sharp decline.

**3.) Distribution Across Temperature Ranges:** This boxplot displays
ridership across various temperature ranges on weekdays and weekends. It
shows that weekday ridership is consistently higher than weekend
ridership across all temperatures, with the most significant difference
in moderate temperatures (50°F - 70°F). Ridership increases slightly as
temperatures rise, with some days having unusually high ridership,
especially in warmer conditions.

**4.) Cluster Analysis of Ridership Patterns:** This scatter plot
visualizes six distinct ridership patterns identified through k-means
clustering. It shows clear peaks during weekday rush hours, with
different clusters dominating these times, indicating high and
consistent ridership. On weekends, ridership patterns are more varied,
with lower overall ridership and a more spread-out distribution
throughout the day.

**5.) Average Passenger Flow of Boarding and Alighting Throughout the
Day:** This line graph compares the average number of passengers
boarding and alighting at different times of the day for each day of the
week. Weekdays exhibit clear peaks during morning and afternoon commute
times, with boarding and alighting patterns closely mirroring each
other. On weekends, ridership is lower and more stable throughout the
day. This graph can inform bus scheduling to better match passenger
demand, especially during peak hours on weekdays.

### $$Clustering and dimensionality reduction$$ {#clustering-and-dimensionality-reduction}

**Description**

This project analyzes the chemical properties of 6,500 bottles of Vinho
Verde wine from northern Portugal to explore whether these properties
can naturally distinguish between red and white wines and differentiate
their quality levels. The analysis utilizes several unsupervised
learning techniques, including Principal Component Analysis (PCA),
t-Distributed Stochastic Neighbor Embedding (t-SNE), and K-Means
clustering, to uncover patterns in the data. The goal is to determine if
these techniques can reveal clusters that align with the wine’s color
and quality, providing numerical and visual evidence to support these
findings.

**Results**

The analysis aimed to determine if the chemical properties of 6,500
Vinho Verde wines from northern Portugal could distinguish between red
and white wines and classify wines based on quality. The following
methods were applied:

-   **t-SNE Analysis**: The t-SNE plot effectively separated the wines
    into red and white categories, revealing well-defined clusters with
    some overlap where wines shared similar chemical profiles.
    Subclusters were observed, which could indicate different quality
    levels within each wine color. However, the overlap suggests that
    wine quality is subjective, as expected given that the ratings were
    provided by a panel of individuals. For instance, higher quality red
    wines tended to cluster in a specific region, while higher quality
    white wines clustered centrally.

-   **PCA Analysis**: The PCA results showed a clear distinction between
    red and white wines, with the first principal component capturing
    most of the variance related to wine color. However, PCA did not
    produce distinct clusters based on wine quality, especially for
    white wines, though red wine quality clusters were somewhat more
    separated.

-   **K-Means Clustering with PCA**: By applying PCA before K-Means
    clustering, the dataset’s dimensionality was reduced, enhancing
    clustering accuracy. The clustering revealed that chemical
    properties effectively group wines into red and white categories,
    though some overlap existed where chemical profiles were similar.
    The clusters aligned with the expected colors and also provided
    insights into quality differentiation, particularly at the extremes
    of the quality spectrum.

### Conclusion

The analysis demonstrated that unsupervised techniques like PCA, t-SNE,
and K-Means clustering could effectively differentiate between red and
white wines based on their chemical properties. While the distinction
between wine colors was clear, the differentiation based on quality was
less distinct, particularly for wines with mid-range quality ratings.
The findings suggest that chemical properties are strong indicators of
wine color, with more nuanced patterns emerging for quality, reflecting
its subjective nature

### $$Market segmentation$$ {#market-segmentation}

**Description**

The analysis of Twitter followers for the consumer brand “NutrientH20”
aimed to gain insights into its audience and identify market segments.
By applying PCA, t-SNE, and K-Means clustering, the study uncovered
seven distinct clusters, each representing different areas of interest.

**Results**

The analysis of NutrientH20’s social media audience identified seven
distinct market segments using t-SNE visualization and K-means
clustering:

**Cluster 0:** Comprises low-activity users who show minimal engagement,
suggesting the need for more engaging content to boost interaction.

**Cluster 1:** Features users with balanced but moderate engagement
across various categories, indicating that diverse content covering
health and leisure might resonate with them.

**Cluster 2:** Consists of health-conscious users with a strong focus on
fitness, suggesting that marketing related to health and fitness would
be particularly effective.

**Cluster 3:** Includes family-oriented users and sports enthusiasts,
who are likely to respond well to content emphasizing family values,
sports, and community activities.

**Cluster 4:** Made up of politically active users, this group may
engage more with campaigns aligned with social causes or political
movements.

**Cluster 5:** Primarily consists of entrepreneurs and small business
owners, who would likely respond well to business-related content
tailored to their interests.

**Cluster 6:** Focuses on fashion, beauty, and personal appearance,
making this segment ideal for marketing fashion and beauty products or
collaborating with influencers in these areas.

In **conclusion**, these segments present unique opportunities for
NutrientH20 to tailor its marketing strategies, enabling the brand to
better connect with its diverse audience and drive growth in specific
demographics.

### $$The Reuters Corpus$$ {#the-reuters-corpus}

**Description:**

For the Reuters C50 text corpus, we used TF-IDF vectorization and
hierarchical clustering to analyze a plethora of documents from
different authors

**Write Up**

**Question:**

Can the documents in the Reuters data be clustered together in a
*meaningful* way based on their content? And what can we learn about the
documents?

**Approach:**

First, we obviously load in the data and we use two variables per
dataset, as we need to store the text itself and the labels (authors) of
that data.

Next, we preprocess the data, in a sense making the data usable. First,
we create a for loop which will run through each text. This for loop
will tokenize the text (seperate the text by words, puncutation, etc).
Then, we remove any stop words or puncuation, and finally stem the words
(convert running to run, etc).

Now we take each word, and convert it to TF-IDF structure. Words that
are common among a couple of documents but rare across the entire corpus
will have high TF-IDF scores. Having a numerical value to compare our
words against each other is necessary for clustering, and TF-IDF gives
more insight than just the overall counts

I then created a dendrogram, which visualizes all the clusters.
Originally, I had set it to go as deep as possible, and then messed
around and adjusted the p value to see where/how many clusters I wanted
to stop at. This diagram is a great way to visualize how the data is
split, and how many documents are within each cluster

However, although I might have wanted 7 clusters, or 9, etc, When I
moved on to the fcluster part of the code (the code which produces the
cluster) and messed around with the t value (how to cut the dendrogram
for each cluster) I ran into an issue. When I started out with a small
amount of clusters, say at t=6 I could create 8 clusters, BUT one
cluster contained 1600 documents! This was way more compared to the 100
or so each other contained, which told me we didn't have enough clusters
to accurately classify the data. Finally, I got to a t=3 value, which
produced 66 well distributed clusters (biggest was only 240)

I then got the number of documents within each cluster, got the authors
which resided in each cluster, clusters per author, and finally got the
10 most common words per cluster.

**Results:**

**Part 1**

*Part 1 of analysis simply looks at which authors appeared in what
clusters.*

Something we can do, is look at the authors found within each cluster.
Some authors had clusters all to themselves! Heather Scoffield, Robin
Sidel, Roger Fillion (x2!), Patricia Commins, Simon Cowell, and Michael
Conner all had clusters to themselves! This indicates that perhaps these
authors have a unique writing style OR (what I think is more likely)
they discussed a unique topic. Later we can look at the top ten most
common words.

Although these authors did have their own clusters, no author appeared
in a cluster only once which is something intresting to consider.

I checked Matthew Bunce, as he appeared in the least amount of clusters,
only two. Each cluster was intresting. He appeared in cluster 50, which
is second largest cluster with 189 documents and in another cluster
which contained 5 other authors and 50 documents. Cluster 51 and 50 (two
largest clusters) I consider to be clusters that are more general, and
capture documents of which there really wasn't a big pattern too, so for
Matthew Bunce, it may be best to only look at his other cluster, cluster
62.

Some authors appeared across *many* clusters, the most top 3 being Mark
Bendeich at 11, and both Brad Dorfman and Scott Hillis at 12. This
indicates that perhaps these authors have a variety of writing styles or
topics.

**Part 2** *Looking at word counts in clusters*

This part of the results is fascinating. By looking at each cluster
individually, we can find common themes within them, as well as by using
command f, find common themes across a variety of clusters.

**Cluster 1:** Included words like China, British, and the word
handover. The inclusion of the word 'handover' to me sounds like it may
have to do with the British handover of Hong Kong to China after WW2!

**Cluster 2:** Also includes, China, however this time it includes words
like legislature, democracy, committie, and provisonal. This to me seems
like it clusters documents regarding Chinese law and legislature.

**Cluster 7:** Included words like 'gm' (General Motors), workers, UAW,
Strike, Plants, and Union. This clearly indicates that cluster 7
includes documents about the UAW strike against General Motors.

**Cluster 9:** Included words like Scotland, bank, analyst, banking,
pence, customers, percent, etc. This indicates it may have to do with
the banking system in Scotland, or something like that

**Cluster 38:** Included words like drugs, Colombia, police,
extradition, government, states, and united. This probably has to do
with Colombian drug cartels, and extraditions possibly to the states

With Command F, we find that some words are common throughout clusters,
like China, market(s), banking, and said. This gives us perhaps an idea
of common themes throughout parts of the corpus. Said is something I may
look to exclude in the future, as it is included in most of the clusters
(however, it does give information. It tells me that the authors are
observing other entities).

Finally, I will look at clusters with just one authors, to see what I
find.

**Roger Fillion:**

Cluster 31 - Top words: fcc, phone, local, carriers, distance, rules,
companies, etc. FCC stands for federal comunications Commision, which
regulates interstate and international communications. Once this is
understood, the other words begin to make sense

Cluster 35 - Top words: tv, ratings, industry, shows, children, content,
parents, valneti, etc. This seems to be discussions regarding tv
ratings, and the industry or genre within the industries.

Super interesting that by looking at the content within these clusters
by the same author, we get absolutely different results which tell
different stories. This suggests our clustering did some great work!

**Robin Sidel:**

Cluster 28 - Top words: conrail, csx, norfolk, southern, offer,
shareholders, bid, stock, cash, etc. Conrail and CSX are rail companies
in the United States, which give us some context about what the
documents may be about. Shareholders, bid, stock, and cash give us
indications that something business related is happening between the two
companies or something like that.

When using command F, I could not find any other clusters who contained
Conrail, CSX, or a similar topic.

There is still *A LOT* more that we could have analyzed, and so much
more that can be learned from this clustering

I also included the final dendrogram used, with the 66 clusters. Can be
found in **Reuters Corpis Ipynb.** The x axis contains the number of
documents, and the y represents the distance's.

### $$Association rule mining$$ {#association-rule-mining}

**Description**

An analysis of a groceries data set was performed using Association Rule
Mining to identify patterns in purchasing behaviors. Then, patterns and
associations discovered where then transformed into Gephi. First, we
interpreted a couple of subsets based off of a general graph. Part I is
analyztion of certain rules based off of 3-D graphs comparing support,
confidence, and lift. Part II is interpretation of Gephi graph

\* note: the graphs used to pick the all subsets can be found in
**Associations Rule Mining PDF**

**Support 0.05% and above**

A big difference between this data set and the playlist data set is how
frequently items appear. In this data set, the support at 0.05% only
draws 34 rules (appears in 5% of baskets or more). Of these rules, 28 of
them are just an item by itself! This gives us insight into the grocery
shopping of individuals and suggests people have very different grocery
shopping lists. Besides these 28 items, there is a lot of diversity in
what people buy.

These 28 items included: canned beef, coffee, beef, napkins, pork,
newspapers, domestic eggs, butter, fruit/vegetable juice, pastry,
bottled water, soda, yogurt, rolls/buns, other vegetables, milk, etc.

These are very common food items, so it makes sense that they appear
constantly throughout the data. Milk has the highest support of 25%,
which makes sense as our graph earlier had milk as the most common food
item.

The other rules included:

yogurt --\> whole milk

other vegetables --\> whole milk

rolls/buns --\> whole milk

and the opposites of these as well! Notice that these are the top 3
items that appeared across all baskets, and their lifts stay between 1.2
to 1.5. This suggests that these associations are not at all powerful,
and their appearance here is more than likely because they appear
throughout all baskets, not because they have associations with each
other.

The difference between the grocery data and playlist data is why in the
first graph above, I choose a support of 0.001 and confidence of 0.01. I
wanted to capture many rules (graph captured 39,000 rules!), so I could
find interesting patterns and then look at the subsets.

**Confidence 75% and Above**

When looking at confidence of 75% and above, we find there are 458
rules. This is interesting, as it represents the probability of the
right-hand side showing up based on what is in the left-hand side.
However, we may run into an issue. If something is very common like
milk, there is a chance that most products will have a high confidence
when milk is on the right side! This doesn't necessarily indicate a
strong association!

Therefore, when looking for rules it is better to just look at the lift
(which tells us how much *more likely* an item is to be bought if it
appears with another and accounts for the frequency of the right-hand
side).

However, some of the 458 rules with confidence above 75% include:

Citrus fruit, fruit/vegetable juice, grapes --\> tropical fruit (lift of
8!)

Frozen meals, tropical fruit, yogurt --\> whole milk (lift of 3)

When looking through the 75% confidence rules, my hypothesis came out
true! As I scrolled down, the majority of the right-hand side was milk!
and the lift was around 3 on average for those which contained milk,
suggesting that these rules weren't very meaningful. A similar pattern
was discovered for other vegetables.

I included above one rule which had a lift of 8 (suggesting it is
genuinely strong!) and one rule with milk on the right-hand side and a
lift of 3.

Notice that for the first rule, the foods make sense to be bought
together. Clearly, the person is buying things to make something fruity!
However, for the milk rule, notice that frozen meals, tropical fruit,
yogurt, and then milk don't really create an interesting meaningful
rule. Rather, it seems to be a conglomerate of random things.

**Lift 10+**

When looking at a lift above 10 (i.e., if item on left-hand side
appears, the item on the right-hand side is 10 times as likely to
appear), we find 78 rules. I decided on the number ten based on insights
from the graph, and when we look at these 78 rules together, we find
foods/items that tend to go together! For example:

Softener --\> detergent (lift: 10)

Popcorn, soda --\> salty snack (16)

Ham, bread --\> cheese (lift: 22)

Bottled beer, red/blush wine --\> liquor (35)

and much more!

These rules make *way* more sense than just looking at the confidence.
It has found associations between cleaning products, alcohol, popcorn,
and sandwich purchases that make perfect sense and by intuition are
quite common!

Something else I noticed is that quite a few of the rules are 2-3 items
together and the inclusion of a 4th. A lot of times this 4th item
doesn't have as close of an association with the other items, BUT it is
considered a necessity, such as:

Butter, root vegetables, and whole milk --\> rice

I personally do not necessarily see a connection with these foods,
however they are considered essential household foods. Perhaps, when we
get rules like these, it suggests that when people buy a lot of food,
they tend to buy many necessities, etc.

#### Part II

By using the Gephi tutorial within the professor's github, **we get a
beautiful graph which can be referenced in the pdf file for Association
Rule Mining**. Gephi discovered 6 communities within the data! Gephi
also got their share of all the data:

Purple: 27% Green: 25% Blue: 25% Orange: 12.64% Dark Green: 6.9% Pink:
2.3%

The graph is an association network, so in short terms it represents
items that are bought together. They may indicate common ingredients,
styles of food, necessities, etc. Something which worried me at first,
was how small the whole milk node is. it is in the purple group, below
the butter. I was concerned, as it was the most frequent item but was
small in the results. However, I believe this is due to what was
discussed earlier: frequency **does not** necessarily indicate strong
association.

**Individual Nodes**

Look at the large nodes, like root vegetables, butter, white break,
tropical fruit, etc. These are nodes that have lots of strong
associations for many other products. As the nodes get smaller and
further away, these have less associations and the associations are
weaker.

Root vegetables for example, are bought often with oil, citrus fruit,
fruit/vegetable juice, herbs, rice, other vegetables, etc. This can be
determined by looking at the arrows and which directions they point in
(although it is a little tough to do)

Another node or community we can look at, is sugar. Based off of the
arrows, we can determine that flour, baking powder, margarine, domestic
eggs, salt, and roll products have strong associations with sugar and
with each other (whenever their arrows point at each other). However,
something like roll products and salt, although they are in the same
community, don't have an association.

**Communities**

We have already covered two communities, green (root vegetables) and
dark green (sugar). The items within each group do seem to corespond to
each other, and the identity of these communities makes sense.

The orange community also seems to make sense. Whipped/sour cream,
yogurt, curd, cream cheese, sliced cheese do make a lot of sense
together and are relatable! On the outskirts, we see smaller
associations which do still make sense, just not as much and only with
specific other items. For example, deserts, cereal, meat spread, coffee,
etc. Notice how these only have a couple arrows pointing at them. Coffee
only has one! What this has taught me is that the further away/smaller a
point is from the middle of the group, the less relatable and less often
it is bought with those things

The community which makes the most sense and is especially specific is
pink, which only contains softner and detergent. The lift was 10, and
the confidence was 90%, so them being together and their own category
makes sense

Two communities I found to be broad were the purple and blue
communities. Some things don't necessarily make sense to be a part of
the same community. For example, in purple, napkins, butter, hamburgers,
and chocolate are all in the same group! In order to understand it
better, you must take a look at where the arrows are going and which
arrow is touching which. If you look closely, napkins and hamburgers do
**NOT** have a lie drawn towards each other, even though they are
particularly large nodes in the same community. Rather, they connect
with nodes within the same community, and have sort of their own subsets
of associations. For example, hamburgers has sauces and instant food
products nearby, with suaces only connected to hamburgers.

You can also find another sub community in purple, cat food and pet care
products.

The blue community also has a lot of sub communities, for example:

Popcorn, salty snacks, soda Bread, processed cheese, ham Bottled beer,
liquor, red/blush wine

My personal favorite, there are connections between soda and liquor!
Could this be jack and coke?

In the future, I would love to dive further and understand why the blue
and purple communities have strange associations. I would also like to
perhaps include even more communities!

### $$Image classification with neural networks$$ {#image-classification-with-neural-networks}

**Description**

The project is focused on image classification using neural networks,
specifically a Convolutional Neural Network (CNN). The goal is to
classify images from the EuroSAT dataset, which consists of various
satellite images categorized into 11 different classes. The images were
preprocessed by resizing them to 64x64 pixels and normalizing them. The
dataset was split into training (80%) and testing (20%) sets.

The neural network model, named SimpleCNN, consists of three
convolutional layers, each followed by a ReLU activation function and a
max-pooling layer. The network ends with two fully connected layers,
with the final layer outputting probabilities across the 11 classes.

**Results**

**Model Performance:** The model achieved an accuracy score of
**88.65%** on the test set, which indicates a good level of accuracy for
this image classification task.

**Top-3 Accuracy:** The model achieved a top-3 accuracy of 98.50%,
meaning that in 98.50% of the cases, the correct class was among the top
3 predictions made by the model.

**Confusion Matrix:** The confusion matrix (both normalized and
unnormalized) was generated to analyze the classification performance
across different classes. The model performed best in identifying images
from the classes SeaLake, Residential, and Forest. However, it struggled
with classes such as Herbaceous Vegetation, Permanent Crop, and River.

**Classification Report:** A classification report was generated,
showcasing the precision, recall, and F1-score for each class. This
detailed analysis helps in understanding the strengths and weaknesses of
the model across the different categories.

The project successfully demonstrates the application of a simple CNN
architecture for image classification tasks, achieving promising results
on the EuroSAT dataset. ​

## 4. Installation/Requirements

-   [Python](https://www.python.org/downloads/)
-   [R](https://cran.r-project.org)
-   [Jupyter Notebook](https://jupyter.org/install)
-   Related libraries: Refer respective files for detailed information.

## 5. File Descriptions

-   **`Q1-Probability`** `contains R code`
-   **`Q2-Data-Wrangling`** `contains R code`
-   **`Q3-Visual-Story-Telling-Green-Buildings`**
    `contains Juptyer Notebook`
-   **`Q4-Visual-Story-Telling-Part-II-Capital-Metro-Data`**
    `contains R code`
-   **`Q5-Clustering-and-dimensionality-reduction`**
    `contains Jupyter Notebook`
-   **`Q6-Market-Segmentation`** `contains python code`
-   **`Q7-The Reuters Corpus`**`contains Juptyer Notebook`
-   **`Q8-Association-Rule-Mining`** `contains R code`
-   **`Q9-Image classification with neural networks`**
    `contains python code`

For detailed information on solutions to each question please refer to
the notebooks and markdown files.

## 6. Contributors/Team

1.  Sarah Dominguez
2.  Mauro Cardona Reyes
3.  Sidarth Saha
4.  Destin Blanchard
