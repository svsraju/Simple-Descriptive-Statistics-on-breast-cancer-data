# Simple-Descriptive-Statistics-on-breast-cancer-data

## Dataset Details

The bc_dataset is a dictionary with multiple fields:

* data : m by n numpy array of the n observed feature values, for each of the m samples
* target : m by 1 numpy array of samples' classification as either malignant (i.e. 0) or benign (i.e. 1)
* target_names : 2 by 1 numpy array of the possible tumor classifications
* DESCR : string containing a detailed description of the dataset
* feature_names : n by 1 numpy array of the names of the feature variables
* filename : string containing the absolute path to where the file containing all the data information is located on the local system

Not all available data is necessary or useful for making predictions and classifying observations. There are numerous feature selection algorithms that exist. For now we are going to arbitrarly select mean radius, mean area, mean concavity, and mean symmetry as our predictor variables. We will not yet be performing any predictions in this Project; rather this term is used to conveniently distinuguish this subset of features from the full set of features

Feature Column Indices
The values observed for each feature resides within a particular 
column of the feature matrix, X. For example, column 0 contains the 
values of the mean radius for each observation, the column at index 
3 contains the values for the mean area, and so on.

I have selected <i>mean_radius_idx, mean_area_idx, mean_concavity_idx, mean_symmetry_idx</i> as predictors of our target. I have not worrked on developing models for this dataset. I have choosed these variables to look in to their distributions.

## BASIC BOXPLOTS OF FEATURES

Boxplots or box-and-whisker plots are used to obtain a perspective of the distribution of the data. The box within the figure displays the 25th percentile (Q1), the median, and the 75th percentile (Q3) of the data. The range between the 75th percentile value and the 25th percentile value is the interquartile range (IQR = Q3 - Q1). The end of bottom line is Q1 - 1.5 * IQR. The end of top line is Q3 + 1.5 * IQR. Anything beyond the lines, the circles, are suggested outliers.

![image](https://user-images.githubusercontent.com/46058709/73568216-9a3b0e00-442d-11ea-9fcb-3c57f89bdd66.png)

## FEATURE CORRELATIONS
It's useful to know the correlation between various features, as well as each feature and the predicted label. Feature correlation is useful for feature selection and understanding the relationship between multiple variables within a dataset. Correlation is either positive, negative, or zero. When two features increase simultaneously, they are positively correlated. When one feature increases while the other decreases, the features are negatively correlated. Zero correlation is when there is no relationship between the features. Correlation is on the range -1 (perfect negative correlation) and 1 (pefect positive correlation).
We can construct scatter plots of one feature versuses another to observe linear or nonlinear relationships.

![image](https://user-images.githubusercontent.com/46058709/73568439-0289ef80-442e-11ea-9022-deedb63bd7a3.png)

## Finding Pearson Correlation

I have created a clormap plot of the correlations between the all the predictors and the target

![image](https://user-images.githubusercontent.com/46058709/73568572-4e3c9900-442e-11ea-8b71-71e3d981d5d7.png)
