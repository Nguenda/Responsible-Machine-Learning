# RML_Group3 Model Card
## **Final Project for Responsible Machine Learning**


### Model Details: Basic information about the model.

The model's purpose is to identify mortgages that have significantly higher APRs compared to the market estimate. The model aims to provide transparency by flagging mortgages that may impose higher costs on borrowers. By predicting high-priced mortgages, the model can contribute to increasing awareness and understanding of the potential financial implications for borrowers.

* **Contributors:** <br>
**Agnes Nguenda**, agnesdanielleflore.nguenda@gwmail.gwu.edu <br>
**Arij Ahmed Khan Lodhi**, arijahmedkhan.lodhi@gwu.edu <br> 
**Kerry McKeever**, kerry.mckeever@gwu.edu <br>


* **Model date:** July 1, 2023
* **Model version:** 1.0
* **Softwares used to implement our best remediated model:** Google Colab, Python 
* **Software version:** **3.10.12**
* **Best remediated model type:** Explainable Boosting Machine 
* **Information about training algorithms, parameters, fairness constraints or other applied approaches, and features:**

  An EBM model was trained using the following parameters initially:
  ExplainableBoostingClassifier(interactions=16,outer_bags=4,max_interaction_bins=64,max_bins=512, early_stopping_rounds = 100,       learning_rate = 0.05, min_samples_leaf = 10, random_state=12345)

  There were some underlying biases in the data which were reduced using debiasing techniques and AIR for the variables was maintained between the range 0.8 to 1.25:

  Adverse impact ratio for Asian people vs. White people: 1.160
  Adverse impact ratio for Black people vs. White people: 0.804
  Adverse impact ratio for Females vs. Males: 0.957

* **State the columns used as inputs in your group’s best remediated model**
 ```   
    ['term_360',
 'conforming',
 'debt_to_income_ratio_missing',
 'loan_amount_std',
 'loan_to_value_ratio_std',
 'no_intro_rate_period_std',
 'intro_rate_period_std',
 'property_value_std',
 'income_std',
 'debt_to_income_ratio_std']
```
* **State the columns used as targets in your group’s best remediated model**
```    
    'high_priced'
```    
* **State the hyperparameters or other settings of your group’s best remediated model**
```    
    ['max_bins': 512,
'max_interaction_bins': 200,
'interactions': 50,
'outer_bags': 8,
'inner_bags': 0,
'learning_rate': 0.01,
'validation_size': 0.25,
'min_samples_leaf': 5,
'max_leaves': 2,
'early_stopping_rounds': 100.0,
'n_jobs': 4,
'random_state': 12345]
```
* **MIT License**

Copyright (c) 2023

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Comments or questions regarding this model can be forwarded to @agnesdanielleflore.nguenda@gwmail.gwu.edu, arijahmedkhan.lodhi@gwu.edu, and @kerry.mckeever@gwu.edu. 


### Intended Use:  Use cases that were envisioned during development.

* The business value of our best produced model is to ensure an unbiased and reliable method to decide whether mortgages should be granted to different housing applicants. This both benefits the consumers, who are able to purchase houses, as well as lenders, who are ensuring they are choosing patrons who will pay back their loans in a timely manner and be an add value to the company.

* The best produced model (EBM) should be used when there is ample applicant information, including but not limited to: debt to income ratio, loan amount, loan to value ratio, property value, income, and demographic information. 

* Our intended users for this model are people with all demographic backgrounds, as out model accounts for these differences and the biases that may be associated with them in previous loan models.

* No further uses for this model are currently known.  


### Factors

The model's performance was analyzed across a variety of relevant factors.

* **Relevant factors:** 

The performance of a mortgage prediction model may vary depending on several salient factors. These factors include demographic or phenotypic groups, environmental conditions, technical attributes, and other domain-specific considerations. Additionally, the quality and relevance of the training data, the selection of appropriate features, the model's ability to handle biases and promote fairness, and its generalization to new and unseen data also play crucial roles. Thorough consideration and analysis of these factors, along with careful evaluation during development and testing, are essential to ensure accuracy, fairness, reliability, and transparency in predicting high-priced mortgages and providing actionable insights to borrowers. Addressing these factors helps create a robust and effective mortgage prediction model that increases awareness about potential financial implications while ensuring reliability and fairness. 

* **Evaluation factors:** 

The evaluation factors reported for the mortgage prediction model include demographic groups, feature selection, handling biases, and the model's performance on new and unseen data. These factors were chosen because they are critical in ensuring accuracy, fairness, and reliability in predicting high-priced mortgages. The evaluation takes into account demographic groups to assess potential biases and disparities. Feature selection is evaluated to ensure the model captures relevant factors affecting mortgage pricing. Handling biases is crucial to promote fairness and avoid discriminatory practices. Lastly, evaluating the model's performance on new and unseen data tests its ability to generalize and provide accurate predictions in real-world scenarios.

By considering and addressing these factors, the mortgage prediction model can provide transparent and actionable insights to borrowers, increase awareness about potential financial implications, and ensure reliability and fairness in predicting high-priced mortgages.


### Metrics: Metrics should be chosen to reflect potential real- world impacts of the model.

* **Model performance measures:** What measures of model perfor- mance are being reported, and why were they selected over other measures of model performance?
  
    * **Accuracy:** The proportion of correct predictions. It is a common and straightforward measure, particularly for balanced datasets.

    * **Precision:** The ability of the model to correctly identify positive cases. It focuses on minimizing false positives.

    * **Recall (Sensitivity or True Positive Rate):** The ability of the model to correctly capture all positive cases. It emphasizes minimizing false negatives.

    * **F1 Score:** The harmonic mean of precision and recall, providing a balanced measure that considers both false positives and false negatives.

    * **Area Under the ROC Curve (AUC-ROC):** The performance of the model across various thresholds, providing a measure of the trade-off between true positive rate and false positive rate.

* **Decision thresholds:** If decision thresholds are used, what are they, and why were those decision thresholds chosen?

* **Variation approaches:**  How are the mea- surements and estimations of these metrics calculated? For ex- ample, this may include standard deviation, variance, confidence intervals, or KL divergence. Details of how these values are ap- proximated should also be included (e.g., average of 5 runs, 10-fold cross-validation). 


### Training Data

* The source of training data was the Home Mortgage Disclosure Act (HMDA) data.   
* The training and test data data was provided to us already spliced into training and test data for educational instructional purposes. 
* The provided training and test datasets contained 160338 rows and 23 columns together. 
* Relevant training data columns
  * **high_priced:** Binary target, whether (1) or not (0) the annual percentage rate (APR) charged for a mortgage is
150 basis points (1.5%) or more above a survey-based estimate of similar mortgages.
  * **conforming:** Binary numeric input, whether the mortgage conforms to normal standards (1), or whether the
loan is different (0), e.g., jumbo, HELOC, reverse mortgage, etc.
  * **debt_to_income_ratio_std:** Numeric input, standardized debt-to-income ratio for mortgage applicants.
  * **debt_to_income_ratio_missing:** Binary numeric input, missing marker (1) for debt to income ratio std.
  * **income_std:** Numeric input, standardized income for mortgage applicants.
  * **loan_amount_std:** Numeric input, standardized amount of the mortgage for applicants.
  * **intro_rate_period_std:** Numeric input, standardized introductory rate period for mortgage applicants.
  * **loan_to_value_ratio_std:** Numeric input, ratio of the mortgage size to the value of the property for mortgage
applicants.
  * **no_intro_rate_period_std:** Binary numeric input, whether or not a mortgage does not include an introductory
rate period.
  * **property_value_std:** Numeric input, value of the mortgaged property.
  * **term 360:** Binary numeric input, whether the mortgage is a standard 360 month mortgage (1) or a different
type of mortgage (0).
  * **Row_id:** unique number assigned to that applicant
  * **Black / Asian/ White/ Amind/ Hipac/ Hispanic/ Non hispanic/ Male/ Female:** demographic identifiers  
  * **Agegte62:** age, greater than 62
  * **Agelt62:** age, less than than 62

*State details of the distribution over various factors in the training datasets.
![image](https://github.com/arijlodhi/RML_Group3/assets/111535170/65979138-a6d4-4a70-b7cb-bc240efeece9)


### Evaluation Data: Details on the dataset(s) used for the quantitative analyses in the card.

* **Datasets used to evaluate the model:**
  * [hmda_train_preprocessed.zip](https://github.com/arijlodhi/RML_Group3/blob/main/hmda_train_preprocessed.zip)
  * [hmda_test_preprocessed.zip](https://github.com/arijlodhi/RML_Group3/blob/main/hmda_test_preprocessed.zip)
* **Source of evaluation (or test) data**
These datasets (both train and test) are real US mortgage data made available through the home mortgage disclosure act (HMDA). 
* **Motivation:** Why were these datasets chosen?
The datasets provide actual mortgage loan information, reflecting real lending practices and patterns. They are highly relevant for assessing ML models in mortgage tasks. The HMDA dataset covers a significant portion of US mortgage activities, offering a representative sample from diverse financial institutions. It enables accurate model evaluations, ensures transparency, accountability, and identifies biases in lending practices. Evaluating models on this dataset detects unintended biases and serves as a benchmark in the industry. Compliance with regulatory requirements is ensured by evaluating models on the HMDA dataset, used by financial institutions and lenders.
* **Preprocessing:** 
The data (both train and test) was preprocessed to remove any obvious data quality problems.
* **State the number of rows in evaluation (or test) data** <br>
  Train data rows = 112253, columns = 23 <br>
  Validation data rows = 48085, columns = 23 <br>
  Test data rows = 19831, columns = 22 <br>
* **Differences in columns between training and evaluation (or test) data** <br>
Column not appearing in the test dataset: 'high_priced'.


###  Quantitative Analysis: Quantitative analyses should provide the results of evaluating the model according to the chosen metrics, providing confidence interval values when possible. 

* The metrics used to evaluate your group’s best remediated model

    * **Accuracy:** 0.9013
    * **Precision:** 0.6032	
    * **Recall:** 0.0159
    * **F1 Score:** 0.0310
    * **Area Under the ROC Curve (AUC-ROC):** 0.8200

* The values of the metrics for training, validation, and evaluation (or test) data – evaluation (or test) metrics come from the most recent class full evaluation results, link under Assignment 1.

    * **ACC**	0.895
    * **AUC**	0.818
    * **F1**	0.404
    * **LOGLOSS**	0.273
    * **MSE**	0.082

* Unitary results: How did the model perform with respect to each factor?
![unitary1](https://github.com/arijlodhi/RML_Group3/blob/main/simulated%20data.png)

* Intersectional results: How did the model perform with respect to the intersection of evaluated factors?

  **Correlation Heatmap**
  
  ![correlation_heatmap](https://github.com/arijlodhi/RML_Group3/assets/112020574/c1f6ab9b-8d19-4185-a796-8cd0f0f05390)

There is significant correlation observed among the variables in the dataset, highlighting interesting relationships. For instance, the **property_value_std** and **loan_amount_std** exhibit a significant positive correlation, which intuitively aligns with expectations. Additionally, it intriguing to note the strong negative correlation between **conforming** and both **loan_amount_std** and **property_value_std**.

Nevertheless, there are two variables, namely **debt_to_income_ratio_std** and **income_std**, that do not show significant correlations with the majority of other variables in the dataset.

* Provide at least one plot or table from each weekly assignment for a total of at least six plots,
that must include the global variable importance and partial dependence of your group’s best
remediated model.

![feature_importance](https://github.com/arijlodhi/RML_Group3/assets/112020574/29211828-040a-44da-81d2-82e528444b54)
* **10th Percentile**
  
![local_feature_10thperc](https://github.com/arijlodhi/RML_Group3/assets/112020574/6e3efea0-c0e6-4934-af40-63fb7551f4b4)
* **50th Percentile**
  
![local_feature_50thperc](https://github.com/arijlodhi/RML_Group3/assets/112020574/a4e6b0a4-644b-4141-8bda-016c0657563f)
* **90th Percentile**
  
![local_feature_90thperc](https://github.com/arijlodhi/RML_Group3/assets/112020574/779ae350-acfc-4eae-82d6-bc7a0b71c458)

![partial_dependence_property_value_std](https://github.com/arijlodhi/RML_Group3/assets/112020574/04cf1b7b-1150-4c11-aa23-18d2890d5b52)

![partial_dependence_loan_to_value_std](https://github.com/arijlodhi/RML_Group3/assets/112020574/72476eef-92f4-42ad-81a8-72d7f0cc645f)

![partial_dependence_income_std](https://github.com/arijlodhi/RML_Group3/assets/112020574/e2349d5e-48c6-4cba-93c1-76d4a5caeb5f)

* Address other alternative models considered

### Ethical Considerations

* Despite our best remediation efforts, there is still a possibility of disparate impact on certain groups based on protected attributes such as race, gender, or ethnicity. We have to address the possibility that the model unintentionally perpetuates historical biases or systemic discrimination present in the training data. Additionally, there may be limitations of the data itself, such as quality and lack of representation. This can impact the performance and fairness of the model. If the training data is incomplete, biased, or lacks diversity, the model's predictions may not accurately generalize to new cases. Lastly, the remediated model may still produce inaccurate predictions for certain cases. False positives or false negatives can occur, leading to wrong decisions and potentially causing harm to individuals. 
* There are many potential math or software problems that could affect our model. Data imbalance, for example, occurs when there is a significant difference in the number of samples between different classes or outcomes, such as approved and rejected loans. Imbalanced data can lead to biased model training and poor performance on the minority class. Additionally, the process of choosing relevant and informative features is crucial for building an effective mortgage model. However, identifying the right set of features and transforming them appropriately can be challenging.
* There are many real world risks involved when deploying a machine learning model. With a biased or incorrect model, those affected include, but are not limited to: mortgage applicants, lenders, underwriters and regulators. The decisions that are made present another risk, as deserving parties may be denied loans, receive incorrect rates,  assess creditworthiness, or allocate resources. The timing of the decisions presents another peril. For instance, if the model makes real-time decisions, the risks may be different compared to a batch-based decision-making process. Real-time decisions can have immediate impacts, while batch decisions may have cumulative effects over time. How decisions are made includes understanding the inner workings of the model and its decision-making process. The risks here include the choice of algorithms, feature selection, model training, and validation procedures. Further, the risks of data privacy and security cannot be overlooked, as the danger of data breaches, unauthorized access, or misuse of personal data are present. 
* Describe any unexpected or results encountered during training.

Overall, our dataset provided no major surprises during the sorting and training of the model. We were previously aware of the biases present in the housing loan process so unfortunately, none of the statistically significant results surprised us.

### Caveats and Recommendations

This section should list additional concerns that were not covered in the previous sections. <br>
* The results don't suggest any further testing. However, bias testing was not performed for the groups 'agegte62', 'agelt62', 'hispanic', and 'non_hispanic'. Therefore, we recommend to perform additional bias testing specifically targeting these groups to ensure fairness and identify any potential issues. 
* Based on the absence of bias testing for certain groups, it is advisable to exercise caution when using the model for decision-making or implementing it in real-world scenarios. Without complete information on bias and fairness, the model's predictions and outcomes may be influenced by hidden disparities or unintended biases. Consider further investigating and refining the model to ensure fairness and mitigate any potential biases identified through bias testing.
* An ideal evaluation dataset should be representative of the population and cover a wide range of demographic groups, including 'agegte62', 'agelt62', 'hispanic', 'non_hispanic', and other relevant categories. It should include a sufficient number of samples from each group to enable accurate and reliable assessments of model performance. Additionally, the dataset should incorporate ground truth labels and detailed information about the loans.


## Collaboration
During the project, we fostered a collaborative environment and utilized effective communication channels to ensure smooth collaboration. We primarily communicated through regular team meetings, both in-person and online, where we discussed project progress, shared updates, and addressed any issues or concerns. Additionally, we maintained open communication channels through instant messaging platforms and email for day-to-day interactions.

To divide tasks, we initially assessed each team member's strengths, interests, and areas of expertise. Based on this assessment, we allocated tasks accordingly, considering the individual's skills and workload balance. We aimed for a fair distribution of responsibilities and ensured that each team member had the opportunity to contribute and develop their skills.

In terms of conflict resolution, we encouraged open and respectful discussions when disagreements arose. We actively listened to each other's perspectives, sought common ground, and worked towards finding mutually agreeable solutions. In case of significant conflicts, we sought the guidance of our project advisor or faculty member to help mediate and provide guidance for resolution.

Overall, our collaborative approach, effective communication, task allocation, and conflict resolution strategies allowed us to work efficiently as a team, leverage our collective strengths, and successfully complete the project.
