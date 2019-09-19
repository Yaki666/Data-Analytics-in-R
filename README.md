# Data-Analytics-in-R


This is the homework of *Data Analytics* taught by [Professor Parker](https://engineering.dartmouth.edu/people/faculty/geoffrey-parker) at Dartmouth College. The course covers the basic techniques and thoughts of data analysis and statistical methods. It's taught in R language and focused on the application of driving insights from data and communicate the results with the audience.

There are four sections: Exploratory Data Analysis (EDA) and Visualization with ggplot, Linear Model, Logistic Regression and Introduction to Machine Learning. Each secion is under the folder which has the problem statement, the solution in R markdown file and the solution in PDF, and data sets used for the analysis. 

You can take a look at the PDF of how I approached to answer the questions from data and more than welcome to play around with the code in R Studio. I was thinking about migrating all the code to Jupyter Notebook, which would benefit reproducibility and interactive learning.

## EDA and Visualization 
The first step of data analysis is to explore the dataset including general statistics, checking null values, general trend, correlation etc. The AirBnB price dataset is used as an example to showcase data visualization with ```ggplot```, which is a powerful package to produce aesthetically high-quality visualizations. ```tidyverse```package was used to wrangle and clean the data. 

## Linear Model
Linear models are simple, easy, naive statisticall method invented a century ago. But it is the **easy-to-interpret** model and the first model you should go to before applying much more complex ones when you are trying to explore what factors are contributing to the result. I had a discussion with a Google employee once, who pioneered the work of classifying Youtube videos. Guess what did he use? Bingo, a linear regression, but with hundreds of thousands of features. The idea behind the linear model is very intuitive, which is to use the description users uploaded to classify the videos. The dependent variable is the the class while independent variables are the frequencies of each word. The trick is how to conduct dimensional reduction and regularization. It performed well and the accuracy was higher than 90%. Later, he used the model to tag more videos and used the dataset to train other complex models. Of course, now we have neural networks such as LSTM to train on the videos itself but still these methods are computation demanding and could not perform very well when hunmans want to cheat it on purpose. This is just a perfect example of solving a complex problem from scratch and iterate to more advanced solutions. 

Again, most people would forget the assumption of linear regression, which is independent normally ditributed variables. We tested normality with hypothesis testing and ```qqplot``` with R in our case. Another trick is to evaluate different regression models, which is covered by R square, AIC/BIC(kind of similar to the concept of regularization). Stepwised regression (significant feature selection) is also introduced.

## Logistic Regeression 
Also, the easiest method to solve a predictive classification problem but it's userful. The underlying linear relationships among variables can explain their importances with regard to the final prediction. This is why people should use these methods. You can interprete the results and make decisions to drive business values in most cases. ```glm``` package in R provides very easy API to run the logistic regression. We also discussed how to seperate the datasets into training and testing and deal with **categorical values** in R.

## Introduction to ML 
Different from statistical methods such as linear and logistic regression (which are part of machine learning most of the time), Machine Learning focuses more on the ability to extract patterns from a large amount of information and predict the outcome rather than the interpretability (decision tree is regarded as a more interpretable model than others but the splitting condition just does not make sense sometime). 

In our credt card default analysis case, the (boost)tree, random forest tree methods and how to use confusion matrix to measure the accuracy of the prediction are introduced. The ```caret``` package in R provides decent numbers of ML methods to build predictive models and as the saying goes: *There is no free lunch*, which is a theory in ML which basically indicates we do not really know what method is the best until we have tried them all!! This starts to sound like experimental science now, which is very interesting and exciting for a data scientist to go through trial and error and have some intriguing discovery finally!


