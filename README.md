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

### \[Probability practice\]

**Description:** - In our analysis, we utilized the Rule of Total
Probability to determine the proportion of truthful respondents
answering “yes” in a website survey scenario (Part A). Following this,
we applied Bayes’ Theorem to evaluate the probability of disease
presence given a positive test result, factoring in both the test’s
sensitivity and the prevalence of the disease (Part B).

**Conclusions/Results:** \* The fraction of people who are truthful
clickers answered yes is 71.43%. The probability of someone having
disease given that they tested positive is 19.89%

### \[Wrangling the Billboard Top 100\]

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

### \[Visual story telling part 1: green buildings\]

**Description**

The project investigates the financial impact of green certification on
commercial rental properties. Specifically, it examines whether green
buildings command higher rents than non-green buildings. The analysis
uses a dataset containing 7,894 commercial rental properties, with 685
of them being green-certified. The main variable of interest is the
median rent per square foot per year, which is compared between
green-certified and non-green buildings.

**Results**

-   **Median Rent for Green Buildings:** $27.60 per square foot per year

-   **Median Rent for Non-Green Buildings:** $25.00 per square foot per
    year

-   **Rent Premium for Green Buildings:** $2.60 per square foot per year

The results indicate that green-certified buildings command a rent
premium of $2.60 per square foot per year compared to non-green
buildings.

**Conclusion**

The analysis concludes that there is a positive rent premium associated
with green-certified commercial buildings. This suggests that tenants
are willing to pay more for properties with green certifications, likely
due to benefits such as energy efficiency, sustainability, and possibly
better work environments.

### \[Visual story telling part 2: Capital Metro data\]

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

### \[Clustering and dimensionality reduction\]

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

### \[Market segmentation\]

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

### \[The Reuters Corpus\]

**Description:**

For the Reuters C50 text corpus, we used the LDA (Latent Dirichlet
Allocation) model to identify key themes in the text. Based on these
themes, we created a mini search engine that suggests authors based on
topics entered by the user, making it easier to explore the dataset.

**Part 1: Initial Clustering Analysis:**

The first part of the analysis focused on clustering the authors based
on their writing, without using TF-IDF scores. Several authors, such as
Heather Scoffield, Robin Sidel, Roger Fillion, Patricia Commins, Simon
Cowell, and Michael Conner, each had clusters unique to them, suggesting
either a distinct writing style or a focus on unique topics.
Interestingly, no author appeared in just one cluster, indicating some
diversity in their writing or topics. Some authors, like Mark Bendeich,
Brad Dorfman, and Scott Hillis, appeared in numerous clusters, with Mark
Bendeich in 11 clusters and the latter two in 12, suggesting versatility
in their writing.

**Part 2: Clustering with TF-IDF Scores:**

In the second part, TF-IDF scores were used to identify common themes
within each cluster:

**Cluster 1:** Focused on topics related to the British handover of Hong
Kong to China, with key words like “China,” “British,” and “handover.”

**Cluster 2:** Appeared to cluster documents related to Chinese law and
legislature, with words like “legislature,” “democracy,” and
“committee.”

**Cluster 7:** Centered around the UAW strike against General Motors,
with key terms like “gm,” “workers,” and “strike.” Cluster 9: Focused on
banking in Scotland, including words like “Scotland,” “bank,” and
“analyst.”

**Cluster 38:** Related to Colombian drug cartels and extraditions, with
terms like “drugs,” “Colombia,” and “extradition.” Some common words,
such as “China,” “market(s),” and “banking,” appeared across multiple
clusters, indicating recurring themes throughout the corpus.

**Author-Specific Clusters:**

**Roger Fillion:**

-   **Cluster 31:** Focused on communications, particularly related to
    the FCC and phone carriers.

-   **Cluster 35:** Related to TV ratings and industry discussions.

**Robin Sidel:**

-   **Cluster 28:** Focused on business dealings involving U.S. rail
    companies Conrail and CSX.

The analysis demonstrated the effectiveness of the clustering, as
clusters from the same author revealed different topics, indicating that
the clustering method successfully captured distinct themes within the
corpus. The final dendrogram included 66 clusters, showcasing the
document distribution and distances between them, providing a
comprehensive overview of the clustering results.

***Conclusion***

The analysis confirmed that clustering documents using TF-IDF can
meaningfully organize them, revealing authors’ writing styles, genres,
and content similarities. This method can be applied to a broader set of
documents to uncover trends in markets, international affairs, and more,
providing valuable insights for investors, CEOs, and other stakeholders.
The clustering tool created is a powerful way to organize and interpret
data, aiding in informed decision-making.

### \[Association rule mining\]

**Description**

An analysis of a groceries dataset was performed using Association Rule
Mining to identify patterns in purchasing behaviors.

**Results**

The Gephi tutorial was utilized to analyze the data, resulting in the
identification of six distinct communities within the network. These
communities represent different groups of items that are frequently
bought together, potentially indicating common ingredients, food styles,
or other necessities.

**Community Breakdown:**

Purple: 27% of the data

Green: 25% of the data

Blue: 25% of the data

Orange: 12.64% of the data

Dark Green: 6.9% of the data

Pink: 2.3% of the data

### **Insights:**

**Association Network:**

-The graph represents an association network where items that are bought
together are connected. The size of the nodes indicates the strength and
frequency of associations.

-Surprisingly, some frequently purchased items like whole milk appear as
smaller nodes, suggesting that frequency alone does not determine strong
associations.

**Notable Nodes:**

-Larger nodes like root vegetables, butter, white bread, and tropical
fruit have many strong associations with other products.

-Smaller nodes are less connected and have weaker associations, often
located further from the core of their community.

**Community Examples:**

**Green (Root Vegetables):** Includes strong associations with oil,
citrus fruit, herbs, and rice.

**Dark Green (Sugar):** Strong associations with flour, baking powder,
margarine, domestic eggs, and salt, though not all items within the
community are directly associated.

**Orange:** Contains related items such as whipped cream, yogurt, curd,
and sliced cheese, with smaller, more specific associations like deserts
and coffee.

**Pink:** Represents a very specific community with only softener and
detergent, having high confidence and lift values, justifying their
close association.

**Purple & Blue:** These communities are broader and contain multiple
sub-communities with less obvious connections, such as hamburgers with
napkins in purple or popcorn with salty snacks and soda in blue.

**Observations & Future Exploration:**

The purple and blue communities have some unusual associations that
aren’t immediately obvious. There is an interest in further exploring
why certain items are grouped together and possibly refining the
analysis to identify even more communities.

### \[Image classification with neural networks\]

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
