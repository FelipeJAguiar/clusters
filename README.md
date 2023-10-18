# VEIGH - CUSTOMER SEGMENTATION

<img src="https://raw.githubusercontent.com/felipejaguiar/clusters/main/image/veigh1.png" alt="logo13" style="zoom:80%;" />

#### This project was based on e-commerce dataset and made by Felipe Aguiar. All context about company are fictitious.

# Business Problem
The Veigh Company is an e-commerce that sells products from different brands. The company has been in business for 2 years and registred a relevant growth. Looking for opportunities gaps, in a dailly meeting, the marketing team realized the importance of understanding the Veigh's costumers that are more representative to company. They want to agroup their customers to create a fidelity program, customizing business actions to each group. So Marketing Team asked Data Team for help to complete this task and:  

👉 Provide a customer segmentation to build a fidelity program.

# Business Assumptions
Business assumptions made were divided in two topics: 

1 - Provide a database including each customer, their specific group and attributes; 

2 - Provide a group’s dashboard analysis; 

3 - The number of group must respect business limitations (3-6 groups);

4 - Answer the questions below:

   🟪 Which group is most important to the company?
   
   🟪 How many costumers will be part of the main group?
   
   🟪 Which revenue’s percentage the most important group represents?

   🟪 What are the attributes of the main group?

 
# Solution Strategy

 ### What is the solution?
 Clusterization of customers by their behaviours.
 
 ### How to provide the solution?
Building a database that include each customer, their specific group and atributes, and their analysis with a dashboard on Metabase.  

### Strategy to solve this challenge was:

The method used to base the solution project was CRISP cicle, adopting some steps to it. Below, the CRISP steps defined.

Steps explained:

1️⃣ Data Description: Analyse descriptive statistic, data types, NA values, null values, dataset dimensions and others data attributes;

2️⃣ Data Filtering: Filter dataset useless rows and/or columns;

3️⃣ Feature Engineering: Modify data values and creating new feature to improve the model; 

4️⃣ Exploratory Data Analysis: Explore dataset to understand variables impact. Look for univariate (each variable), bivariate (relations between two variables) and multivariate (correlation between all variables) analyses;

5️⃣ Machine Learning Modelling: Train machine learning models, analysing the space study with dimensionality reducers and evaluate it with metrics;  

6️⃣ Hyperparameter Fine Tunning: Find the parameter (k = number of clusters) that results in the best value;

7️⃣ Clusters Analysis: Analyse the results to improve business values;

8️⃣ Deploy of Results: Create a database and a dashboard of clusters analysis on metabase. 

# Machine Learning Model Applied and Results

Some clusterization models were tested to obtain the best solution. The models choosed were: Hierarchical Clustering, Gaussian Mixture Model and K-Means.
First of all, the solution was distributed in steps, being the first a basic clusterization named RFM (Recency, Frequency and Monetary, where some groups are created based on three these attributes) to introduce a basic solution before the complex;  the forward steps were developing the complex solution, studying how to improve the model and increase value.

<img src="https://raw.githubusercontent.com/felipejaguiar/clusters/main/image/veighd.png" alt="logo23" style="zoom:20%;" />

Font: Author (2023)

Talking about "final result", an important study about dimensionality reducer contributed to solve this business problem and have a better understanding of clusterization problems. Were used PCA (Principal Component Analysis), UMAP, T-SNE and Tree Based Embedding looking for a better data clusterization and visualization.
Following the business limitation was chosed 6 as a number of groups (k), so the results are to k=6.
Below, the results of machine learning algorithms based on Silhouette Score (a metric that analyse the distance between points of data and clusters):
   

|Model Name		      |KMEANS		 |GMM  	|HC  |
|--------------------|------------------|-------------|-----------------|
|Not Reducer 	               |0.72	          |0.59        |0.71            |
|UMAP 	|0.59             |0.47        |0.59            |
|t-SNE			|0.33	          |0.29        |0.29            |
|Tree Based Embedding	      |0.41 	          |0.32	      |0.40            |

*Silhoute Score values ranges -1 to 1 (closer to 1, better).

By the table, the best metric was for the algorithm KMeans with not dimensionality reducer.

# Business Results

The results os segmentation were obtained and some of principals charecteristics are in image below.

<img src="https://raw.githubusercontent.com/felipejaguiar/clusters/main/image/veigh card.png" alt="logo14" style="zoom:60%;" />

Font: Author (2023)

Cards give to us a general analyse of each cluster. The “TOP” group is “Cluster 2” with the best number for all atributes. The groups “Lost A” and “Lost B” represents customers that bought few products, lost contact and not buy for almost a year. Group “Rescue” means an opportunity of rescue some costumers that bought often but for a random reason stopped buying. They are a relevant percentage of costumers and have sizable atributes values. According their numbers, "Ascending" are customers that have a great chance of transforming into “Veighers” in the future. “Improve”, like “Asceding”, are a group with potential to raise their status but in a lesser level.       

The final clusters dataset was uploaded to a database in MongoDB (NoSQL) to feed Metabase, create clusters and general data visualizations, checking one of business assumptions.   

<img src="https://raw.githubusercontent.com/felipejaguiar/clusters/main/image/dashveigh1.PNG" alt="logo20" style="zoom:50%;" />
<img src="https://raw.githubusercontent.com/felipejaguiar/clusters/main/image/dashveigh2.PNG" alt="logo21" style="zoom:50%;" />

* Red = bad value; Yellow = regular value; Green = good value.

# Top 3 Veighers Insights

<b>Hypothesis 01</b>: Veighers represents 30% of total revenue.

❌FALSE: Veighers represents 39.12% of total company’s revenue.

<b>Hypothesis 02</b>: Veighers, Ascending and Improve gross revenue, represents 80% of total gross revenue.

❌FALSE: The more representative clusters (Veighers/Ascending/Improve) represents 70% of total gross revenue.

<b>Hypothesis 03</b>: Veighers represents 25% of total purchases.

✅TRUE: Veighers represents 27% of total purchases, even more than the hypothesis.

# Conclusions

Finally, all the questions and the business problem were solved and answered by the built model, indicating the best structure to create a fidelity program. Now, the marketing team is able to elaborate a strong plan and implement specific actions for each costumers  group.
This project could help the company to solve business question and find opportunities to increase earnings through Data Science techniques. Besides it, was a big chance to develop my Data Science knowledge, learning about different machine learning algorithms, dimensionality reducer, metrics and tools. 

# Next Steps to Improve

 - Automate the process of colect and segmentation;
 - Try others clusterization algorithms;
- Expand dimensionality reducers and space studies;
 - Search and build new features to feed the model with e-commerce metric like Customer lifetime-value, Click-through rate, Conversion rate;
- Build a forecast model about each cluster.
 
# References

Loyalty programs: https://www.zendesk.com.br/blog/loyalty-rewards/#georedirect

E-commerce metrics and KPI's: https://thegood.com/insights/ecommerce-metrics/

Dimensionality reduction: https://towardsdatascience.com/reducing-dimensionality-from-dimensionality-reduction-techniques-f658aec24dfe

# <b>Tools:</b>

<a href = "www.python.org"><img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" target="_blank"></a>
<a href = "www.jupyter.org"><img src="https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter" target="_blank"></a>
<a href = "https://www.mongodb.com"><img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" target="_blank"></a>

