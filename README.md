### Project Title

EPA range predictior for Electric Vehicles

**Author**
Usman Tariq

#### Executive summary
- [Executive Summary](https://github.com/usman-tariq77/Capstone-Project-24.1-Final-Report/blob/main/Executive%20summary.docx)


#### Rationale
Why should anyone care about this question?

A good model will help reduce the dependency on physically testing EVs and bring the expected information closer to design time. So manufacturers can test and validate different features in the design phase compared to building prototypes and testing physically. 

#### Research Question
What are you trying to answer?

Predicting EPA ranges of Electric cars based on features and data that impacts the range (battery size, drag coefficient, size of the car etc.)
A good model will help reduce the dependency on physically testing EVs and bring the expected information closer to design time. So manufacturers can test and validate different features in the design phase compared to building prototypes and testing physically. 

#### Data Sources

[First data source](https://afdc.energy.gov/vehicles/search/results?view_mode=grid&search_field=vehicle&search_dir=desc&per_page=8&current=true&ajax_count=18&fuel_id=41&category_id=27,25,29,9&all_manufacturers=y) for EV info.
Remainder of the information can be obtained through each manufacturers press releases and specification info.

#### Methodology
What methods are you using to answer the question?

I had originally thought of using Logistic Regression, KNN Classifierer, DecisionTree Classifier and SVM but those are all classifiers so had to pivot to using models that work with range of numbers like Linear Regression, SVR, Decision Tree Regressor, KNN Regressor. 

In the second pass I also included the Ensemble technique using Random Forst, Bagging and Gradient Boosting for validation as well. Out of all the models I tried and validated using the best parameters the list of Regressors came down to Decision Tree and Random Forest. While Decision Tree was faster the Random Forest had better performance.
The train/test split was 80/20, using onehot encoding on the categorical columns, removing all the NA data. 

#### Results
What did your research find?

Based on the tested models Ensemble technique with Random Forst seems to yield the best results. Using GridSearchCV the best hyperparameters are model__max_depth: None, model__min_samples_leaf: 1, model__min_samples_split: 2, model__n_estimators: 200. Using the hyperparameters we can predict the EPA ranges of EVs with the provided features.

The most important features that impact the range were:
* Battery capacity
* Drag coefficiency (aerodynamics)
* Curb weight

#### Next steps
What suggestions do you have for next steps?

There are a few items that are next:
1. Validate with some more data to ensure the model provides the expected outcome
2. Deploy the model for use for the teams that are designing the product to ensure they can utilize the learnings to plan the future models better
3. Continue to collect data from more EVs to refine the model
4. Model can be adapted to provide MPGe guidance to support modeling for future efficiency regulations


#### Outline of project

- [Link to notebook](https://github.com/usman-tariq77/Capstone-Project-24.1-Final-Report/blob/main/EV.ipynb)


##### Contact and Further Information

Contact info: Usman Tariq

