# Challenge20-credit-risk-classification
In this project we create a logistic regression model which helps us to predict a credit risk for a bank based on customer's profile.
If we provide the input (customer's information) for the model with: 'loan_size', 'interest_rate', 'borrower_income', 'debt_to_income', 'num_of_accounts', 'derogatory_marks', 'total_debt', we will receive recommendation for the approval for the loan (`value_counts` = 0 (positive)) or decline (`value_counts` = 1 (negative)).
Initially we operated with the original data (77536 rows) splitting it into training and testing variables; the evaluating results for this model are:
1. Accuracy = 0.9918 (the chance that the prediction will be correct based on the model),
2. Precision (negative) = 0.8466 (the chance that a not qualified customer will not receive a loan among customers with negative prediction).
3. Recall (negative) = 0.9095 (the chance that a not qualified customer will not receive a loan among not qualified customers). 0.0905 = 1 - 0.9095 can be considered as a risk for a bank to give a loan for a person who is not qualified.
The second model is the logistic regression model with oversampled balanced data where the ratio of positive and negative responses is 1:1 (150072 rows); the evaluating results for this model are:
1. Accuracy = 0.9944 (is better than in the original model),
2. Precision (negative) = 0.9944 (is better)
3. Recall (negative) = 0.9945 (the chance that a not qualified customer will not receive a loan). 0.0055 or 0.55% bank's risk is low for this model.
I would recommend using the balanced model since the risks for a bank are lower here. But I would also recommend playing with a balanced model by taking a more fair ratio such as 10:1 or 5:1 (positive vs negative).
