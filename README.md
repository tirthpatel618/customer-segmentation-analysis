
# Customer Segmentation Analysis

### Project Overview

The objective of this data analysis project is to offer understanding regarding the prime demographic among mall customers to target by performing customer segmentation of specific groups of customers considering various metrics like age, income, and shopping score. The best possible clusters were identified using KMeans unsupervised machine learning algorithm to find the univariate, bivariate, and multivariate clusters. Summary statistics were performed on these identified clusters to identify the best marketing group.

### Data Sources

Mall Customer Data: The primary dataset used for this analysis is the "Mall_Customers.csv" file, containing detailed information about each customer's gender, age, annual income, and spending score (1-100; based on factors like frequency of purchases, amount spent per transaction, etc).

### Tools
- Anaconda - Python Installation (pandas, seaborn, matplotlib, sklearn libraries)
- Jupyter Notebook - Data Analysis

### Exploratory Data Analysis

Univariate Analysis: 
Examining histograms and kernel density estimation (KDE) plots for each metric (age, annual income, and spending score) enabled a comprehensive exploration of the dataset's characteristics. These visualizations facilitated the assessment of frequency/central tendancy, revealing that the most frequent shopper is between 30-40 years old, has an annual income between $50k-$75k, and a spending score between 40-60. The visualizations also provided insight on the shape of the distribution, showing the data was approximately normally distributed.

<img width="436" alt="image" src="https://github.com/tirthpatel618/customer-segmentation-analysis/blob/main/assets/univariate.png">
Figure 1. Example distplot for annual income.


Using the 'hue' parameter to further differentiate the customer base by gender unveiled a predominant representation of female shoppers across the metrics, characterized by denser concentrations in the dataset.


<img width="436" alt="image" src="https://github.com/tirthpatel618/customer-segmentation-analysis/blob/main/assets/gender_univariate.png">

Figure 2. Example KDE plot for annual income, utilizing the hue parameter to distinguish the distributions for both male and female.


Using boxplots for each metric allowed for a detailed examination of the median, quartiles, outlier presence, and data spread, facilitating a comparison across genders.

<img width="425" alt="image" src="https://github.com/tirthpatel618/customer-segmentation-analysis/blob/main/assets/boxplot1.png">

Figure 3. Example boxplot for annual income. Although the median incomes for both males and females are similar, the distribution of female incomes appears to be more varied. Furthermore, an outlier is noticeable within the male income data.

Bivariate/Multivariate Analysis:
Employing scatterplots/pairplots allowed the visual inspection and catorization of clusters in the data. The utilization of the 'hue' parameter helped distinguish between male and female categories so distinct trends can be analyzed between the genders.

<img width="428" alt="image" src="https://github.com/tirthpatel618/customer-segmentation-analysis/blob/main/assets/multivariate.png">

Figure 4. Scatterplot for the relationship between annual income and spending score. Visual approximation identifies 5 clusters.



<img width="632" alt="image" src="https://github.com/tirthpatel618/customer-segmentation-analysis/blob/main/assets/clustering.png">

Figure 5. Pairplot using the 'hue' parameter. Age, annual income, and spending score metrics.


Heatmaps were used to visualize the correlation between the variables. It was noticed that there is a slight negative correlation between age and spending score, sugesting that customers spend less as they get older. Additionally, there is a slight positive correlation between annual income and spending score, suggesting that spending increases as annual income increases.


![image](https://github.com/tirthpatel618/customer-segmentation-analysis/blob/main/assets/heatmaps.png)

Figure 6. Heatmap depicting the correlation between variables.

### Clustering

Centroid-based clustering was employed using KMeans algorithm to group data points around centroid coordinates, where the distance between points and the centroid are minimized. First, the algorithm is fit to the data, then predicted labels were extracted from the fitted model. Since the optimal number of clusters is not explicitly known, the 'elbow' technique is used which involves plotting the inertia, or the within-cluster sum of squares (WCSS), and identifying the 'elbow' or point of inflection in the plot.

![image](https://github.com/tirthpatel618/customer-segmentation-analysis/blob/main/assets/more%20clusters.png)


Figure 7. Plot of inertia (WCSS) vs. number of clusters for bivariate clustering. The point of inflection occurs at n = 5, so this n value is the optimal number of clusters.



![image](https://github.com/tirthpatel618/customer-segmentation-analysis/blob/main/assets/optimal%20clusters.png)


Figure 8. Vizualization of the Spending and Income Cluster. Clusters are distinguished by color, and their central points (centroids) are displayed on the plot.




### Results/Findings

The main analysis results are as follows
- Spending and Income cluster 0 has the highest spending score and highest annual income, and is predominately female (53.85%) with an average age of 32.
- Spending and Income cluster 4 has high spending score, but lowest annual income, and is predominately female (59.90%) with an average age of 25.



