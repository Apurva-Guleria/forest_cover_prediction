# forest_cover_prediction
<!-- Project Title -->
Forest Cover Type Prediction Using Random Forest


<!-- goal -->

the goal of this project is to predict the forest cover type(from 7 categories) based on features like elevation,slope,soil type and wilderness area.

<!-- Data set info -->
Rows-15,120
Columns-56(target column (Cover_type) included )
Source-intership company Unified mantor

Target column: Cover_Type (values from 1 to 7)


<!-- Steps i followed -->
1. In first step i import the libraries and load the data set.
2. print first few rows use of .head() method
3. checks no. of rows and columns with the help of .shape
4. checks the type of data with the use of .info() method
5. than i check any missing value present in the columns
6. than i used df['Cover_Type'].value_counts() to check how many samples belongs to each forest type.
7. than i check column name if any column is unwanted than i will drop
8. Id column is not useful so i drop it
9. separate the features and target
10. train and test split as 80/20%
11. than we have to import RandomForestClassifier from sklearn ensemble module, Random forest is a ensemble model,meaning it builds many decision trees and combines them to make a more accurate and stable prediction.
12. last step is to check accuracy_store,classification_report,confusion_matrix

<!-- what i learn -->
1. i learn to use value_counts() in target column so if any overrepresented and underrepresented classes are prsent or not
2. i learn about randomforest to predict forest cover types based on various features. i learned this model is powerful that build multiple decision trees and combines their result to improve the accuracy. It handles both numerical and binary features without needing any feature scaling. 

<!-- Results -->
Accuracy: 0.8723544973544973
Confusion Matrix:
 [[327  58   0   0  15   0  21]
 [ 74 314  15   0  30   4   1]
 [  0   0 357  20   2  49   0]
 [  0   0   6 441   0   2   0]
 [  1   3   9   0 400   3   0]
 [  0   3  42  13   3 371   0]
 [ 10   2   0   0   0   0 428]]
Classification Report:
               precision    recall  f1-score   support

           1       0.79      0.78      0.79       421
           2       0.83      0.72      0.77       438
           3       0.83      0.83      0.83       428
           4       0.93      0.98      0.96       449
           5       0.89      0.96      0.92       416
           6       0.86      0.86      0.86       432
           7       0.95      0.97      0.96       440

    accuracy                           0.87      3024
   macro avg       0.87      0.87      0.87      3024
weighted avg       0.87      0.87      0.87      3024

<!-- Author -->
 "Apurva Guleria"
ML intern at Unified Mentor
