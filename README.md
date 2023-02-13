# EDA-Haberman-Dataset
## Objective: 
To observe the significance of each feature in the survival or non-survival of patient and to find most significant features by performing Univariate and Bi-variate analysis.

## Observations:
- Here in this dataset, there are 306 rows, 4 columns ( age, year, nodes and status) and 3 features(age,year,nodes). 'status' column has the categorical data and have 2 categories(1,2).All other columns contains variable datapoints. In 'status' column '1' is for patients who survived and '2' is for patients who do not-survived.
- There are 225 patients who have survived 5 years or longer and 81 patients who have not-survived or died within 5 years. This dataset is imbalanced dataset.
- At the age from 30 to 33, everyone has survived. But after 33 chance of non-survival is increasing till age 50.Although the dataset is imbalanced, it can be seen that, at the age 40 to 60 there is proportionately more chance of non-survival of patient than survival.Also after the age 77, there is almost no chance of survival. As the data is imbalanced and most of the plot is overlapping,it is difficult to say that 'age' is the significant feature to classify survivor and non-survivor.
- If 'year' is taken as a feature, it can be seen that most of the plot is overlapped and PDF curves are crossing each other. Although the operation is carried out, there is no certainity of survival of patient within 5 years. It is not possible to classify patients using 'year' as a feature.
- In the range of node between 0 to 5 approximately, chance of survival is proportionately greater than the chance of non-survival. Also as nodes increases chance of survival decreases. Here 'nodes' can be more significant than any other feature to classify because PDF curves are much better seperated than features 'age' and 'year'.

![image](https://user-images.githubusercontent.com/87875987/218484740-f801d80a-7d89-4370-bb47-b532e9d35dd2.png)
- In the above plot Red curve denotes the CDF of survived patients and Green curve denotes CDF of non-survived patients. Both curves are intersecting each other and not well seperated. From age 48 (approx) both survived and not-survived patients have almost the same curve. At age 67 (approx), there are equal percentage of survived and not-survived patients. So using CDF, 'age' feature do not have that much significance in survival or non-survival of the patients.

![image](https://user-images.githubusercontent.com/87875987/218484886-6608f8c2-ebd4-4886-a93a-8635723e78a7.png)
- In the above plot Red curve denotes the CDF of survived patients and Green curve denotes CDF of non-survived patients. Same as the 'age' feature, here, both curves are intersecting each other and not well seperated. Although a different year of operation, patients have the almost equal chance of survival and non-survival. So using CDF, 'year' feature also do not have that much significance in survival or non-survival of the patients.

![image](https://user-images.githubusercontent.com/87875987/218485075-90def628-1aa4-4afb-a54a-8aed6d605a32.png)
- In the above plot Red curve denotes the CDF of survived patients and Green curve denotes CDF of non-survived patients. Unlike 'age' and 'year' feature, here, both curves are very well seperated till node 25. Here it depicts that, having less node gives more certainity of survival than non-survival. At node 15, percentage of survived patients are 95% (approx) and not-survived patients are 85% (approx). So using CDF, 'nodes' feature have much significance in survival or non-survival of the patients than other two features.

![image](https://user-images.githubusercontent.com/87875987/218485338-0661c148-dd10-493e-832d-9aa4a62bf40f.png)
- fig(1)-Feature = age : 25th, 50th and 75th percentile of both survived and not-survived are almost equal. 50th percentile of both classes are age 52 and age 53 (approx) resepctively, which are almost same, but 25th percentile value shows that smaller the age, more is the chance of survival. Still 'age' is not the significant feature as both classes have almost equal quantile values.
- fig(2)-Feature = year : 50th percentile of both the class are at year 63. 25th percentile values shows that year before 60 has the more chance of non-survival, but after year 60, it cannot be well defferentiated as both class have overlapping quantile values.
- fig(3)-Feature = nodes : This figure clearly depicts that node value from 0 to 5 has more chance of survival. Quantile values are diffrerent for each class and not overlapping. Here 75th percentile value shows that almost all the survived patients has the node value less than 5. From the 'nodes' feature, we can very well classifiy the survived and not-survived patients. Therefore 'nodes' is much more considerable feature than other two features.

![image](https://user-images.githubusercontent.com/87875987/218485539-772861a5-c274-4d7b-beef-b840641a5ec1.png)
- Feature 'age' and 'year' has almost same spread/density between certain range. In the fig(3), survived patients shows more spread near to the zero but not-survived patients do not have that much spread in the same range of nodes. This figure very well differentiates survived and not-survived. So 'nodes' is the most significant feature.

![image](https://user-images.githubusercontent.com/87875987/218486212-1d2588a0-a338-46c5-8c9b-ca9f098557fa.png)
- Above 2D scatter plot shows that, if 2 features are used to classify, most of the points overlap each other. Differentiating becomes too hard as between certain range, points from both class (i.e. survived and not-survived) are present in that range. Use of two features makes it difficult to find significane of features and thus classify based on those features.

![image](https://user-images.githubusercontent.com/87875987/218486333-c42c5f1b-3a44-44cc-a2c8-29b1d5501f8e.png)
- If pair plot is considered, nodes and age features combined gives much more seperated points, than any other features combination. Still there are too much overlapping points which will reduces the significance of each other feature.

## Conclusion:
- By performing univariate analysis, it is seen that 'nodes' is much more considerable feature which defferentiate both classes.
- By performing Bi-variate anaylysis, it has been clear that no any features combination can be helpful in the classification.
- 'nodes', a single feature can be very significant in the classifiaction between survived and not-survived.
- Amongst the Univariate and Bi-variate analysis, Univariate analysis is much more useful to find out the significance of the feature in the Haberman Dataset.
