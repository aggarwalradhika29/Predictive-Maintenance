# Predictive-Maintenance
Predictive Maintenance

Data Description:
The dataset consists of 10,000 data points stored as rows with 10 features in columns.
1.	UID - unique identifier ranging from 1 to 10000.
2.	Product ID - consists of a letter L, M, or H for low (50% of all products), medium (30%) and high (20%) as product quality variants and a variant-specific serial number.
3.	Type – indicates the quality of the product as L, M or H.
4.	Air Temperature [K] - generated using a random walk process later normalized to a standard deviation of 2 K around 300 K.
5.	Process Temperature [K] - generated using a random walk process normalized to a standard deviation of 1 K, added to the air temperature plus 10 K.
6.	Rotational Speed [rpm] - calculated from a power of 2860 W, overlaid with a normally distributed noise.
7.	Torque [Nm] - torque values are normally distributed around 40 Nm with a Ïƒ = 10 Nm and no negative values.
8.	Tool Wear [min] - The quality variants H/M/L add 5/3/2 minutes of tool wear to the used tool in the process.
9.	Target - indicates, whether the machine has failed in this particular data point for any of the following failure modes are true.
10.	Failure Type – indicates what type of failure has occurred.


Types of Machine Failures:
1.	Tool Wear Failure: the tool will be replaced of fail at a randomly selected tool wear time between 200 â€“240 mins (120 times in our dataset). At this point in time, the tool is replaced 69 times, and fails 51 times (randomly assigned).
2.	Heat Dissipation Failure: heat dissipation causes a process failure, if the difference between air- and process temperature is below 8.6 K and the tool â€™s rotational speed is below 1380 rpm. This is the case for 115 data points.
3.	Power Failure: the product of torque and rotational speed (in rad/s) equals the power required for the process. If this power is below 3500 W or above 9000 W, the process fails, which is the case 95 times in our dataset.
4.	Overstrain Failure: if the product of tool wear and torque exceeds 11,000 min Nm for the L product variant (12,000 M, 13,000 H), the process fails due to overstrain. This is true for 98 data points.
5.	Random Failure: each process has a chance of 0.1% to fail regardless of its process parameters. This is the case for only 5 data points, less than could be expected for 10,000 data points in our dataset


Machine Learning Algorithms:
Various ML Algorithms have been used in the model out of which the best performing one is selected to further predict and work on testing and creating the report.
ML models employed are:
1. Random Forest
2. Support Vector Machines
3. Linear Regression
4. Logistic Regression
5. Decision Trees
6. K-Nearest Neighbours

Mostly, RF performs the best for prediction on a huge dataset.

If we have noisy or unstandardized data, we can use following techniques to clean and pre-process it:
1. Data Cleaning: Handling missing data, or outliers
2. Data Integration
3. Data Transformation: Scaling, and normalization
4. Data Discretization
5. Data Reduction: PCA, or LDA

Data Visualization can be used for change detection between noisy and cleaned data.
