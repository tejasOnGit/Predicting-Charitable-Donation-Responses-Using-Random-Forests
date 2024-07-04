## Predicting Charitable Donation Responses Using Random Forests

#### Introduction
This repository contains a solution for predicting which individuals are likely to respond positively to charitable donation requests using a Random Forest model. The dataset, `mailing.csv`, originates from a real direct marketing campaign and includes various features related to the individuals' donation history and demographic information.

#### Data Description
The dataset includes the following features for each individual:
- **Income:** Household income
- **Firstdate:** Date associated with the first gift by this individual
- **Lastdate:** Date associated with the most recent gift
- **Amount:** Average donation amount by this individual over all periods
- **rfaf2:** Frequency code
- **rfaa2:** Donation amount code
- **pepstrfl:** Flag indicating a star donator
- **glast:** Amount of the last gift
- **gavr:** Amount of the average gift
- **class:** Outcome variable, 1 if they gave a donation in this campaign, 0 otherwise

#### Project Structure
The project follows a structured approach to analyze the data, build a predictive model, and evaluate its performance. The main steps are:

1. **Data Exploration and Preparation:**
   - Assess the distribution of the `class` variable in both training and test datasets to ensure balance.

2. **Model Fitting:**
   - Fit a Random Forest model using the training dataset.
   - Determine the out-of-bag (OOB) error rate for the model.

3. **Predictive Performance Evaluation:**
   - Compute the confusion matrix and various performance metrics using the `confusionMatrix` function.
   - Create ROC plots and compute the Area Under the Curve (AUC) for both training and test datasets.

4. **Model Examination:**
   - Examine the variable importance scores from the Random Forest model.
   - Make individual predictions using the model and analyze the impact of key features.

5. **Impact Analysis:**
   - Use Individual Conditional Expectation (ICE) and Partial Dependence Plots (PDP) to understand the influence of key features on donation predictions.

6. **Summary and Recommendations:**
   - Summarize the model’s predictive performance and key findings on feature importance.
   - Discuss potential improvements and provide recommendations for future campaigns.

#### Summary of Findings
- The initial data exploration indicates that the `class` variable is relatively balanced between the training and test datasets.
- The Random Forest model shows varying performance on training and test datasets, with potential overfitting observed during evaluation.
- Key features impacting donation predictions include income, donation dates (Firstdate and Lastdate), and past donation amounts.
- Adjustments to model complexity and regularization techniques may improve predictive accuracy.

#### Recommendations
- Simplifying the model or using regularization techniques may help mitigate overfitting.
- Collecting more data can enhance the model's generalization capabilities.
- Tailoring solicitation strategies based on key features such as income and past donation behavior may improve campaign success.

#### Usage
To replicate the analysis:
1. Load the dataset and required libraries.
2. Run the provided code to fit the Random Forest model and evaluate its performance.
3. Use the model to make predictions and analyze the impact of key features.

#### Bonus: PDP+ICE Chart
The repository also includes a bonus section demonstrating the use of the `iml` package to create a Partial Dependence Plot (PDP) combined with Individual Conditional Expectation (ICE) curves. This helps visualize the effect of specific features on the predicted probability of donation.

#### Conclusion
This project provides a comprehensive approach to building and evaluating a Random Forest model for predicting charitable donation responses. The insights gained can help improve future marketing campaigns by targeting individuals more effectively.

---

Feel free to explore the notebook and modify the code as needed to fit specific requirements or datasets. Contributions and suggestions are welcome!

---

#### Files in the Repository
- **NoteBook.ipynb:** Jupyter notebook containing the full analysis and model development.
- **mailing.csv:** Dataset used for the analysis (not included in this repository, please ensure to have it available in your environment).

---

#### License
This project is licensed under the MIT License - see the LICENSE file for details.

---

Happy analyzing! If you have any questions or feedback, feel free to open an issue or submit a pull request.
