# Floods-Predictive-model-Python
The objective of this project was to create a predictive model that would successfully predict the likelihood of a flood using
the logistic regression based on the monthly rainfall.

## Predictive model to predict flood based on monthly rainfall

![1](https://user-images.githubusercontent.com/107842949/179395927-57aca32c-c1d2-46b7-aaa6-dce6aae8ae51.JPG)
## Exploration of the dataset

![2](https://user-images.githubusercontent.com/107842949/179395982-23725d04-4922-4062-84eb-066913a14473.JPG)
## describe()
The describe() function summarizes the dataset’s statistical properties, such as count, mean, min, and max:

![3](https://user-images.githubusercontent.com/107842949/179396051-5e19c577-27af-4831-9285-177af14da10f.JPG)
## Corr()
The corr() function display the correlation between different variables in dataset

![4](https://user-images.githubusercontent.com/107842949/179396119-a366bd89-f950-4461-acd4-380855f4c56d.JPG)
## Replace
In order to train this python model, we need the values of our target output to be 0 & 1. So, we'll replace values
in the Floos column (YES,NO) with (1,0 respectively)

![5](https://user-images.githubusercontent.com/107842949/179396196-3cfc8361-ea2a-40ff-9fb9-7916e2e727c9.JPG)
## Feature Selection
In this step, we choose several features that contribute most to the target output. So, instead of training the
model using every column in our dataset, we select only those that have the strongest relationship with the
predicted variable.
Use the SelectKBest library to run a chi-squared statistical test and select the top 3 features that are most related
to floods.

![6](https://user-images.githubusercontent.com/107842949/179396249-84cd1bf5-4870-4c36-b82c-4e8f8640b655.JPG)

![7](https://user-images.githubusercontent.com/107842949/179396289-4124abd1-23b1-493b-8c74-d6eaf0dd9c3d.JPG)
## Build the Model
Now it’s time to get our hands dirty. First, split the dataset into X and Y:
![8](https://user-images.githubusercontent.com/107842949/179396293-b0ce4936-8460-4109-a264-4d41e1266b4b.JPG)

![9](https://user-images.githubusercontent.com/107842949/179396526-a75c65ae-e17f-4107-8ff6-ff22b213f3c6.JPG)
![10](https://user-images.githubusercontent.com/107842949/179396576-680b2741-660c-43f8-90b9-ab7c30b635c7.JPG)
## Evaluate the Model's Performance
Now we'll evaluate how well our model performed predictive analytics by running a classification report and a ROC curve
## Classification Report
Classification Report is a performance evaluation report that is used to evaluate the performance of machine
learning models by the following 5 criteria.

Accuracy: is a score used to evaluate the model's performance. The higher it is,the better.
Recall:  measures the model's ability to correctly predict the true positive values.
Precision is the ratio of true positive to the sum of both true and false positives F-score combines precision and recall into one metric. Ideally, its value should be closest to 1, the betterSupport is the number of actual occurrences of each class in the dataset

![11](https://user-images.githubusercontent.com/107842949/179396901-acc454cd-e8b5-4308-89ef-72124f00327e.JPG)
## ROC Curve
The receiver operating characteristic (ROC) curve is used to display the sensitivity and specificity of the logistic
regression model by calculating the true positive and false positive rates
From the ROC curve, we can calculate the area under the curve(AUC) whose value ranges from 0 to 1. You'll
remember that the closer to 1, the better it is for our predictive modeling
To determine the ROC curve, first define the metrics
![12](https://user-images.githubusercontent.com/107842949/179396947-23d05c3d-9356-4174-9e6b-78ff51efc4f7.JPG)
Finally, plot the ROC curve:

![13](https://user-images.githubusercontent.com/107842949/179397030-56f030c5-833f-4f96-b60f-ead1653805b1.JPG)
