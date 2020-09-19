# mantis
##Web Part

Environment setup-

1- Apache Server

2- MySQL

3- Clone the repo

4- Make sure that you clone repo in the folder which is configured with Server

5- Run https://localhost/mantis/index.php/gearup
## Machine learning Part-

Environment setup-

1- Python 3.7.6

2- Python libraries - pandas,numpy,sklearn,pickle,seaborn,matplotlib


# [![mantis1.png](https://i.postimg.cc/4yCgv5TF/mantis1.png)](https://postimg.cc/5YmTb8yw)
# [![mantis2.png](https://i.postimg.cc/bYQcc1Pp/mantis2.png)](https://postimg.cc/238Xnb3K)
# [![mantis3.png](https://i.postimg.cc/282trwKR/mantis3.png)](https://postimg.cc/mt1jSQ48)
# [![mantis4.png](https://i.postimg.cc/mZSXyjRz/mantis4.png)](https://postimg.cc/kDBvnx2q)

Dataset-
Download data from-
 https://www.kaggle.com/michaelacorley/unemployment-and-mental-illness-survey
 

we use Unemployment and mental illness survey data for this project.
Data Analysis-
we have 31 features in our dataset, now we did feature engineering to find the best classifying features.
Correlation is one of the best way to find the relation in the data, the correlation matrix is 
![](ML_Script/correlation.jpg)

Now on we will select some best classifying features and use them in building our model.
Now we have to convert the data of some features from string to integer as most of the ml algorithms don't work well with string data.
For this, we will use Labelencoder.
After Labelencoding we have to standardize our data to make its mean to 0 and variance to 1, for this we use StandardScale .

Now Let's try to use different models as the classifier and select the best one based on the accuracy (recall and precision as well).

after some models, we have a Logistic regression Model as best classifier for this dataset,
Confusion matrix for this model is-
![](ML_Script/confusion_matrix.jpg)

its recall score is-0.875 and precision score is-0.66 with accuracy of 86.56716417910447 on test data.

Now we will save Labelencoder,standardscale and model for using it at deploying time.
