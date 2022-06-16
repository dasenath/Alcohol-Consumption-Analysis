# Alcohol-Consumption-Analysis
**Intent of the program**
The program attempts to analyze the data, tranform the data (using one-hot encoding), perform feature engineering (using Recursive Feature Engineering), build Neural Network and SVM models, train and test the models and visualize the results.

The details of the dataset can be found here "UCI Machine Learning Repository: Drug consumption (quantified) Data Set" https://archive.ics.uci.edu/ml/datasets/Drug+consumption+%28quantified%29

**Key highlights:**

Reduced overfitting and improved the precision of alcohol 'Used Yesterday' class as presented in Figures 1 and 2. The project began with an emphasis on balancing the minority class samples or weight and this can be backed by SVM’s results; however, there was a shift in the notion. NNs, on the other hand, gave better results when not balanced. From this behavior, it can be inferred that it is not necessary to balance the datasets always, but the need for balancing is model-dependent. Balancing of data is not required when the minority class has enough samples that allow the model to identify patterns.

**_Issue 1:_**

_Description:_ The classes in the dataset were heavily imbalanced and overlapped.

_Solution:_ 
1. Merged related classes to create a binary classification problem - Classifying if the patient consumed alcohol yesterday or not.
2. Used SMOTE technique to oversample the data of the minority class.
3. Used class weight balancing technique while training the SVM model.
4. Compared the results for the two balancing technique combinations.

**_Issue 2:_**

_Description:_ Choosing the appropriate metrics for model training as the dataset did not offer features that differentiated the classes well.

_Solution:_ Trained the models by focusing on Precision of the class 'Used Yesterday'.


Figure 1: Comparing metrics for various balancing technique combinations for SVM
![image](https://user-images.githubusercontent.com/105256866/174124606-01d1fea4-f49b-4186-b03a-479f859598e1.png)


Figure 2: Comparing metrics for various balancing technique combinations for NN
![image](https://user-images.githubusercontent.com/105256866/174124737-ec4c49ce-ceaa-46fb-93d7-7b961fd9b207.png)




