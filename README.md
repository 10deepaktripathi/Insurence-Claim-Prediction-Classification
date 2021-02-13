company wants a modal that can predict whether an insured will claim or not. To work on this requirement, we have been provided historical data that contains categorical target “claim status” along with other information related to insured persons in the past.  Claim status is equal to True if insured claimed else it is False. 
I have built a classification modal for this task which I chose after doing comparative study among various other classification modal. Below is a summary on what all I did-


1.	After loading the data file “CE802_P2_Data.csv” first I checked if the dataset is balanced or not and found that it was not highly imbalanced.
2.	After that I described the dataset and found that F15 has half of the missing values. First, I dropped F15 and then trained the modal on remaining data. Second, I included the F15 and imputed the missing values using different approaches (Mean imputation and Model based imputation) and then again trained the models on this data.
3.	Before training models, I divided the data in two splits in the ratio of 80:20. Used K-fold cross validation on train split to compare the scores of various models. Tested the best modal on test split as well. 
4.	Few columns were having slightly different scale from others, so I tried scaling the whole dataset.
5.	I did hyperparameter tunning using Grid Search to get the best performance/parameter of all models.
6.	Tried using deep learning modal (MLP) as well.
7.	Lastly used MLP, which is the best modal as per my analysis, to predict the test dataset provided by the insurance company.
