# kmeans-clustering-for-college-data

In this project, we will explore the use of KMeans Clustering to classify universities into two groups: Private and Public. While we have access to the labels for this dataset, it's important to note that we will NOT use them for the KMeans clustering algorithm. Typically, KMeans is used when we do not have labels, making this an unsupervised learning approach. 

## About the Data

We will work with a dataset containing information on 777 universities. This dataset includes 18 variables:

- Private: A factor with levels No and Yes indicating whether the university is private or public.
- Apps: Number of applications received.
- Accept: Number of applications accepted.
- Enroll: Number of new students enrolled.
- Top10perc: Percentage of new students from the top 10% of high school class.
- Top25perc: Percentage of new students from the top 25% of high school class.
- F.Undergrad: Number of full-time undergraduates.
- P.Undergrad: Number of part-time undergraduates.
- Outstate: Out-of-state tuition.
- Room.Board: Room and board costs.
- Books: Estimated book costs.
- Personal: Estimated personal spending.
- PhD: Percentage of faculty with Ph.D.’s.
- Terminal: Percentage of faculty with terminal degrees.
- S.F.Ratio: Student/faculty ratio.
- perc.alumni: Percentage of alumni who donate.
- Expend: Instructional expenditure per student.
- Grad.Rate: Graduation rate.

## Import Libraries

Let's start by importing the libraries typically used for data analysis.

## Get the Data

We will read in the College_Data file using `read_csv`. We'll also set the first column as the index.

## Exploratory Data Analysis (EDA)

It's time to create some data visualizations! We'll perform the following tasks:

- Create a scatterplot of Grad.Rate versus Room.Board, with points colored by the Private column.
- Create a scatterplot of F.Undergrad versus Outstate, with points colored by the Private column.
- Create a stacked histogram showing Out of State Tuition based on the Private column.
- Create a similar histogram for the Grad.Rate column.
- Correct the graduation rate for a private school that has a rate above 100%.

## K Means Cluster Creation

Now, we'll create the cluster labels. We'll perform the following tasks:

- Import KMeans from SciKit Learn.
- Create an instance of a K Means model with 2 clusters.
- Fit the model to all the data except for the Private label.
- Obtain the cluster center vectors using `kmeans.cluster_centers_`.

## Evaluation

Since we have access to labels in this exercise, we'll evaluate the clusters by performing the following tasks:

- Create a new column for the DataFrame called 'Cluster', which assigns a 1 for a Private school and a 0 for a public school.
- Create a confusion matrix and classification report to assess how well the KMeans clustering worked without being given any labels.

This project demonstrates how KMeans clustering can be used for grouping data without labels and how evaluation metrics can be applied when labels are available, although this is not the typical use case for KMeans.

## Conclusion

The K Means Clustering Project - Solutions provides step-by-step solutions and explanations for applying KMeans clustering to university data. 
