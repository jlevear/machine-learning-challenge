# machine-learning-challenge

## Preprocessing the Data

My first step in this project was viewing and interpreting the data provided. Once I vaguely understood what some of the columns meant, I concluded that I would not be able to select the relevant features myself. My strategy was to create a model using all of the features and then go back and select only the relevant ones. I started by assigning the X features to every column in the dataset except for koi_disposition, which was assigned to the y feature. Then I used the one-hot encoder to change the disposition feature from string values to arrays of numberic values. Next I scaled the X features and separated the data into training and testing data. I did some preliminary analysis by training the model using basic Decision Tree and Random Forest tests. I found that the Random Forest test performed only slightly better (~3%). I assume this was due to overfitting the training data so decided to proceed with Decision Tree for tuning the model parameters. 

* __Model 1 (Decision Tree):__ The first model used GridSearch in conjunction with Decision Tree. 

* __Model 2 (K Neighbors):__ The second model used used Gridsearch in conjunction with K Neighbors. 

## Selecting Relevant Features

To minimize noise and increase the signal of the models, I used a Decision Tree-based estimator to select the relevant features of the dataset. This narrowed the features down from 40 to 7. I was hesitant to use this for my final models because I thought it took away too many features. However, when I reran the tests the accuracy scores remained high, so I decided to keep it for the final models. The final results of Model 1 was 88% accuracy, while the final results of Model 2 was 79% accuracy.

## Conclusion

I am fairly confident that Model 1 could be used to predict new exoplanets, given all the relevant features. While I would hope for higher accuracy, the cost of a false positive is relatively low. If this model was for something that could impact someone's health or safety, than I would require accuracy closer to 100%. If I needed to make this model more accurate, I could try different models with different parameters until I found one that had higher accuracy. Alternatively, I could use the same models with a greater number of highly varying parameters. This method would involve more time and computational resources, however.  


