# <p align ="center"> Credit Card Default Prediction </p>

<p align ="center"><img src="https://user-images.githubusercontent.com/101988419/175786661-5cf93791-d1bb-4c24-8c5d-6b3ff4286848.gif"
     class="centerImage"
     width="500"
     height="300" </p>
   


## 1. **Business Problem**

<p align ="justify"> Credit cards are one of the key business areas within the banking industry, and have gained huge success in the past few years. Banks often issue credit cards to ineligible customers without sufficient background checks in an effort to increase their market share. Additionally, many customers overused their credit cards, resulting in high debt accumulation. One of the biggest challenges banks face is identifying risks and non-risks among customers. So, the problem we are trying to analyze is how to identify the risky and non-risky customers, helping the bank to decide if a customer has the potential to repay the used credit of the bank. < /p>

## 2. **Approach**

●	*Null values Treatment*
     
<p align ="justify"> Thankfully our dataset contains no missing values and duplicate values. so there was no need to remove or impute them. </p>
     
●	*Encoding of categorical columns*
     
<p align ="justify"> We used One Hot Encoding to produce binary integers of 0 and 1 to encode our categorical features because categorical features that are in string format cannot be understood by the machine and needs to be converted to numerical format.</p>

●	*Exploratory Data Analysis*
     
  <p align ="justify"> After loading the dataset we performed this method by comparing our target variable that is “default.payment.next.month” with other independent variables. This process helped us figuring out various aspects and relationships among the target and the independent variables. It gave us a better idea of which feature behaves in which manner compared to the target variable. </p>

●	*Feature Selection*
     
<p align ="justify">In these steps we used algorithms like ExtraTree classifier to check the results of each feature i.e which feature is more important compared to our model and which is of less importance. Next we used ANOVA to select the best feature which we will be using further in our model.</p>

●	*Treating class imbalance (SMOTE)*
     
<p align ="justify"> To compensate for the rare classes in the imbalance dataset, we use SMOTE(Synthetic Minority Over-Sampling Technique) method to over sample the minority class and ensure the sampling is not biased. What this technique does under the hood is simply duplicating examples from the minority class in the training dataset prior to fitting a mode. After SMOTE sampling, the dataset has almost equal size of 0s and 1s.</p>

●	*Fitting different models*
     
For modelling we tried various classification algorithms like:
1.	Logistic Regression
2.	Decision Tree Classifier
3.	Random Forest Classifier
4.	KNN Classifier

## 3. **Result**
     
 ![image](https://user-images.githubusercontent.com/101988419/175787191-07adbbdb-e003-4826-8cfe-1803543d6b02.png)

## 4. **Conclusion**

●	The dataset has 25 features and 30000 records without any missing or duplicated value. But, it has many outliers which were treated using IQR method.

●	The dataset was pretty clean but had imbalanced data which was balanced using SMOTE (Synthetic Minority Oversampling Technique) resampling.

●	EDA was performed to understand the data clearly and finding correlations, like defaulter as per different categories, total bills, reason of negative bill etc. and important features were identified using extraclassifier and ANOVA test.

●	Logistic Regression, Decision Trees, Random Forest algorithms were implemented which were evaluated using ‘Recall’ score.

●	Even after applying SMOTE, there was imbalance in score as well. Logistic Regression had performed well comparatively with recall score of about 83% for class 0 and 56% for class 1. There is scope of furthur optimization.


