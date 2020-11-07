# WineQualityPrediction
White wine quality prediction using Machine learning algorithms
********************************* This is the README txt for running the Jupyter script******************************************************
Requirements:
	Jupyter notebook 
		or
	Colab Google 
		or
	Kaggle
		or
	Any IDE like Atom or Visual Studio Code with ipython kernel installed and enabled jupyter server. (We developed this code using VS code)

Basic Details:

The file name is Wine_Quality_Score.ipynb. (1MB)
Most of the library modules included are already available in scikit, pandas or numpy.
There are two additional modules installed namely seaborn and statsmodel. If you haven't installed it, You can install it by running the command
"pip install <module>" in your shell and then try again.

#Detailed information of the each cell is given in the comment lines of the cell in the .ipynb file.

The steps given below is a brief walkthrough of what the code executes sequentially.
1. Importing the dataset from the file 'winequality-white.csv' and create a dataframe.
2. Seperate the Feature labels and output label separately into X and Y dataframes.
3. Next, we use the SelectKBest feature selection technique from sklearn to identify the k best features given by its algorithm.We have used both chi
test and f-values as score functions.
4. After that, We use the ExtratreesClassifier from sklearn to plot the feature importances of individual features.
5. Correlation matrix for the feature labels is created and heatmap is generated for displaying its importance of each distinct values. Also, relevant
features from the correlation matrix is displayed in the code.
6. Next, we implement the feature selection method using backward elimination and recursive feature elimination techniques respectively. The output of 
both the feature selection methods have been clearly displayed in the code. Additional to the above mentioned methods, We have also used the lasso 
feature selection method.
7. *Sometimes you might encounter an error, "SVD did not converge". This happens because of having more eigenvalues as zero. And that causes the memory run
out. You can clear out the error by running that particular cell once or twice and then it will show the results of that cell.
8. We have been using a scale of 0-10 for the wine quality as Y label. Now, We are gonna redefine it to three different categories: Low, Medium and High.
Low: values less than 5, Medium: values between 5 and 7, High: values above 7.
9. Labelencoder() is used to convert the string values to numerical values for implementing the newly defined scores. 
10. After this step, we are now changing the y label we earlier used for feature selection with the new y label to see if there is any improvement in the
feature selection. Positively the results are optimized and cogent.
11. Then, we split the dataset into training (80%) and testing (20%) for our calculation purposes.
12. The StandardScaler() function is used to preprocess and normalize the X labels by removing the mean from each individual cells of a feature and transform
it to avoid a biased classification.
13. We then, split the new y label values too in the same ratio of 80% training to 20% testing data frames.
14. We have used SVM, GaussianNB, KNeighbors classifer and Decision Tree classifier as classifiers to train our data and generate models to predict similar 
label values for a given data.
15. We use training data to train our data and testing data to test our data. And accuracy score for each classifier model is calculated to find the deviations
from the actual value by comparing the predicted and actual values.
16. Accuracy score and confusion matrix for each classifier model is displayed right after their individual function cell in the code. 
17.Classification report and ROC curve for each of the classifier model for different y labels have been displayed in the output terminal to understand the 
statistical parameters.
