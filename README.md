# Netflix_Movies_and_TV_Shows_Clustering

## Problem Statement

Netflix is the world's largest online streaming service provider, with over 247 million subscribers as of 2023-Q3. It is crucial that they effectively cluster the shows that are hosted on their platform in order to enhance the user experience, thereby preventing subscriber churn.

We will be able to understand the shows that are similar to and different from one another by creating clusters, which may be leveraged to offer the consumers personalized show suggestions depending on their preferences.

The goal of this project is to classify/group the Netflix shows into certain clusters such that the shows within a cluster are similar to each other and the shows in different clusters are dissimilar to each other.

## Attribute Information

- show_id : Unique ID for every Movie/Show
- type : Identifier - Movie/Show
- title : Title of the Movie/Show
- director : Director of the Movie/Show
- cast : Actors involved in the Movie/Show
- country : Country where the Movie/Show was produced
- date_added : Date it was added on Netflix
- release_year : Actual Release year of the Movie/Show
- rating : TV Rating of the Movie/Show
- duration : Total Duration - in minutes or number of seasons
- listed_in : Genre
- description : The Summary description

## Key Features

- Know Your Data: The first step in this project was to examine the various features of the dataset, understand the structure of the data and identify any patterns or trends. We looked at the shape of the data, the data types of each feature, and a statistical summary.
- Exploratory Data Analysis: We conducted an exploratory analysis of the data to identify patterns and dependencies, and to draw conclusions that would be useful for further processing.
- Data Cleaning: We checked for duplicated values in the dataset and then addressed any null values and outliers by imputing empty strings and dropping some of the null rows.
- Textual Data Preprocessing: We used techniques such as stop word removal, conversion to lowercase, lemmatization, tokenization, and word vectorization to prepare the textual data for clustering. We also used Principal Component Analysis (PCA) to handle the curse of dimensionality.
- Cluster Implementation: We used K-Means and Agglomerative Hierarchical clustering algorithms to cluster the movies and determine the optimal number of clusters.
- Content-Based Recommendation System: We built a content-based recommendation system using the similarity matrix obtained from cosine similarity, which will provide the user with 10 recommendations based on the type of movie/show they have watched.


## Conclusion

- The dataset contained about 7787 records with 12 attributes. Initial steps involved addressing missing values within the dataset and conducting exploratory data analysis (EDA).

- It was found that Netflix hosts more movies than TV shows on its platform, and the total number of shows added on Netflix is growing exponentially. Also, majority of the shows were produced in the United States.

- It was decided to cluster the data based on the attributes: director, cast, country, genre, rating,listed_in and description. The values in these attributes were tokenized, preprocessed, and then vectorized using TFIDF vectorizer.

- Through TFIDF Vectorization, we created a total of 10000 attributes.

- We used Principal Component Analysis (PCA) to handle the curse of dimensionality. 3000 components were able to capture more than 80% of variance, and hence, the number of components were restricted to 3000.

- We first built clusters using the K-Means Clustering algorithm, and the optimal number of clusters came out to be 5. This was obtained through the elbow method and Silhouette score analysis.

- Then clusters were built using the Agglomerative clustering algorithm, and the optimal number of clusters came out to be 7. This was obtained after visualizing the dendrogram.

- A content based recommender system was built using the similarity matrix obtained after using cosine similarity. This recommender system will make 10 recommendations to the user based on the type of show they watched.
