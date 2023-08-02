# Classification_Predicting_Purchase
People often spend a lot of time browsing through online shopping websites, but the conversion rate into purchases is low. Determine the likelihood of purchase based on the given features in the dataset. The dataset consists of feature vectors belonging to 12,330 online sessions. 
### Data Description:

The dataset contains the following features:


1. **Administrative** -	Number of pages visited by the user for user account management related activities	Discrete values from 0 to 27 
2. **Administrative_Duration** -	Time spent on Admin pages by the user	Continuous value (time in seconds)
3. **Informational** -	Number of pages visited by the user about the website	Discrete values from 0 to 24
4. **Informational_Duration** -	Time spent on Informational pages by the user	Continuous value (time in seconds)
5. **ProductRelated** -	Number of product related pages visited by the user 	Discrete values from 0 to 705
6. **ProductRelated_Duration** -	Time spent on Product related pages by the user	Continuous value (time in seconds)
7. **BounceRates** -	Average bounce rate of the pages visited by the user	Continuous value 
8. **ExitRates** -	Average exit rate of the pages visited by the user	Continuous value 
9. **PageValues** -	Average page value of the pages visited by the user	Continuous value 
10. **SpecialDay** -	Closeness of the visiting day to a special event like Mother’s Day or festivals like Christmas	Discrete values (0, 0.2, 0.4, 0.6, 0.8, 1.0)
11. **Month** -Month of the visit from Jan to Dec	Categorical
12. **OperatingSystems** -	OperatingSystems of the visitor like windows etc..	Discrete values from 0 to 7
13. **Browser** -	Browser of the visitor like chrome, yahoo etc..	Discrete values from 0 to 12
14. **Region**-	Geographic region from which the session has been started by the visitor	Discrete values from 0 to 8
15. **TrafficType** -	Traffic source through which user has entered the website	Discrete values from 0 to 19
16. **VisitorType** -	Visitor type as New visitor, Returning user or Others	Categorical
17. **Weekend** -	If the user visited on a weekend or not	Boolean
18. **Purchase** -	If the user Purchased / Not	Boolean

19. Based on the analysis of the data set using the Gradient Boosting model, the following conclusions can be drawn:


1. **High Accuracy**: The Gradient Boosting model achieved a high accuracy of 90.4%. This means that the model is making correct predictions for approximately 90.4% of the instances in the dataset. This high accuracy indicates that the model is performing well in classifying the data into the correct classes.

2. **Balanced F1 Score(weighted)**: The weighted F1 score of 90% suggests that the model is reasonably good at maintaining a balance between precision and recall. The weighted F1 score takes into account class imbalances, and a value of 90% implies that the model is effectively identifying both positive and negative instances.Since the accuracy and F1-score are not exactly the same, it suggests that the dataset might be imbalanced, meaning one class has significantly more instances than the other. The model might be performing better on the majority class (higher accuracy) while not as well on the minority class (lower F1-score). In such cases, further investigation and possible handling of class imbalance might be required.

4. **Model Selection**: The results indicate that Gradient Boosting is a good choice for this dataset as it achieves high accuracy and a reasonable F1-score. However, it's essential to compare these results with other models 
* Tunned XG Boosting Classifier	  ----------      Acurracy - 90.376 ---	weighted f1 score - 90.027
* Random Forest Classifier	      ----------      Acurracy - 90.214 ---	weighted f1 score - 89.555
* Support Vector Machine(classifier)  ----------              Acurracy - 90.187	--- weighted f1 score - 89.942
  
  to determine if Gradient Boosting is indeed the best model for this specific problem.

5. **Hyperparameter Tuning**: The model might have the potential to further improve its performance by fine-tuning hyperparameters. The GridSearchCV process used for hyperparameter tuning can be revisited to search for more optimal hyperparameters and potentially improve both accuracy and the weighted F1-score.

6. **Business Impact**: Finally, consider the business implications of the model's performance. Depending on the specific application, accuracy and weighted F1-score might have different levels of importance. Consider the cost of false positives and false negatives and how the model's predictions align with the business objectives.

In conclusion, achieving an accuracy of 90.4% and weighted F1-score of 90% is a promising result, but further analysis, model evaluation, and business context are essential to draw comprehensive conclusions and make informed decisions. 
