# Titanic passenger survival prediction
This project is based on the [kaggle compettion](https://www.kaggle.com/c/titanic) for preditcting if 
a person will survive or not on the Titanic.

# Cleaning the data
The given training data had a lot of issues:
* There was not sufficient data
* Many attributes did not contribute much to he end result so they were removed like:
    * Name of the passenger
    * Cabin of the passenger (many missing values in this one)
    * Emabarked: Where the person boarded the Titanic
    * Titcket: Ticket type of the passanger (varied a lot)
  
* The Age of the person can be a key attribute in predicting wether a person survived or not and it had many missing values and it had to be dealt with.

# Predicting the missing ages
The 'Age' attribute was missing many values and it was a very important attribute in decideing if a 
person had survived or not.

There were 3 ways I could have solved the problem:
* Remove the rows containing missing age values: This was not possible because the total data avialable
was itself less and removing the rows would mean that the data left was next to nothing so this was not an option.
  
* Using statistical methods to fill the missing data: such as using the mean of the ages available to fill the missing values
but doing so would not be appropriate as there may be people of varying ages so this was also not an option.
  
* Creating a modle to predict the missing ages: Now this looks like a good idea! I created a 3 regression models
a linear regressor, decision tree regressor, random forest regressor. After evaluating all the models I found out that 
  they were performing relatively same but the random forest regressor haas a slight edge. I used this model to predict the missing 
  ages in both the train and test set.
  
# Predictions 
I trained 2 models for predicting a persons survival one was a SVDClassifier and the other was a
Random Forest Classifier out of these 2 the random forest classifier had a much better ROC AUC Score
so I used this one to predict if a person would survive or not.

After the predictions were complete I got a score of **75/100** on kaggle and considering from the discussion 
on the competion the highest which can be achicved with this data was about **80** so I think I faired pretty well.

# Conclusion 
With a littile bit tuining to the model I think we can squeez out a lit bit more performance. Due to the lack of data
and insufficient info on the data it would be very dificult to increase the performance of the model above 80%.
None the less this competion helped me understand a lot about data cleaning and classification models.


















