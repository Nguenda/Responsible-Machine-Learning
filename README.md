# RML_Group3 Model Card
## **Final Project for Responsible Machine Learning**


### Model Details: Basic information about the model.

The model's purpose is to identify mortgages that have significantly higher APRs compared to the market estimate. The model aims to provide transparency by flagging mortgages that may impose higher costs on borrowers. By predicting high-priced mortgages, the model can contribute to increasing awareness and understanding of the potential financial implications for borrowers.

* Contributors:<br>
**Agnes Nguenda**, agnesdanielleflore.nguenda@gwmail.gwu.edu <br>
**Arij Ahmed Khan Lodhi**, arijahmedkhan.lodhi@gwu.edu <br> 
**Kerry McKeever**, kerry.mckeever@gwu.edu <br>

#Arij
* Model date: July 1, 2023
  
* Model version: 1.0
  
* State the software used to implement your group’s best remediated model

  Google Colab, Python
  
* State the version of the modeling software for your group’s best remediated model

  3.10.12
* Model type: State the type of your group’s best remediated model

  Explainable Boosting Machine
  
* Information about training algorithms, parameters, fairness constraints or other applied approaches, and features

  An EBM model was trained using the following parameters initially:
  ExplainableBoostingClassifier(interactions=16,outer_bags=4,max_interaction_bins=64,max_bins=512, early_stopping_rounds = 100, learning_rate = 0.05, min_samples_leaf = 10, random_state=12345)

  There were some underlying biases in the data which were reduced using debiasing techniques and AIR for the variables was maintained between the range 0.8 to 1.25:

  Adverse impact ratio for Asian people vs. White people: 1.160
  Adverse impact ratio for Black people vs. White people: 0.804
  Adverse impact ratio for Females vs. Males: 0.957

* State the columns used as inputs in your group’s best remediated model
    
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

* State the columns used as targets in your group’s best remediated model
    
    'high_priced'
    
* State the hyperparameters or other settings of your group’s best remediated model
    
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

* Paper or other resource for more information
  
* Citation details

* MIT License

Copyright (c) 2023

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Comments or questions regarding this model can be forwarded to @agnesdanielleflore.nguenda@gwmail.gwu.edu, arijahmedkhan.lodhi@gwu.edu, and @kerry.mckeever@gwu.edu. 

##Kerry 
### Intended Use:  Use cases that were envisioned during development.

* The business value of our best produced model is to ensure an unbiased and reliable method to decide whether mortgages should be granted to different housing applicants. This both benefits the consumers, who are able to purchase houses, as well as lenders, who are ensuring they are choosing patrons who will pay back their loans in a timely manner and be an add value to the company.

* The best produced model (EBM) should be used when there is ample applicant information, including but not limited to: debt to income ratio, loan amount, loan to value ratio, property value, income, and demographic information. 

* Our intended users for this model are people with all demographic backgrounds, as out model accounts for these differences and the biases that may be associated with them in previous loan models.  (should we add cut offs for incomes/ ages? Ie: The intended user for this model receives an income of over ___ and is over ___ in age?) 

* No further uses for this model are currently known.  

##Agnes
### Factors

Analyzing the model's performance across a variety of relevant factors.

* Relevant factors: What are foreseeable salient factors for which model performance may vary, and how were these determined?

The performance of a mortgage prediction model may vary depending on several salient factors. These factors include demographic or phenotypic groups, environmental conditions, technical attributes, and other domain-specific considerations. Additionally, the quality and relevance of the training data, the selection of appropriate features, the model's ability to handle biases and promote fairness, and its generalization to new and unseen data also play crucial roles. Thorough consideration and analysis of these factors, along with careful evaluation during development and testing, are essential to ensure accuracy, fairness, reliability, and transparency in predicting high-priced mortgages and providing actionable insights to borrowers. Addressing these factors helps create a robust and effective mortgage prediction model that increases awareness about potential financial implications while ensuring reliability and fairness. 

* Evaluation factors: Which factors are being reported, and why were these chosen? If the relevant factors and evaluation factors are different, why?

The evaluation factors reported for the mortgage prediction model include demographic groups, feature selection, handling biases, and the model's performance on new and unseen data. These factors were chosen because they are critical in ensuring accuracy, fairness, and reliability in predicting high-priced mortgages. The evaluation takes into account demographic groups to assess potential biases and disparities. Feature selection is evaluated to ensure the model captures relevant factors affecting mortgage pricing. Handling biases is crucial to promote fairness and avoid discriminatory practices. Lastly, evaluating the model's performance on new and unseen data tests its ability to generalize and provide accurate predictions in real-world scenarios.

By considering and addressing these factors, the mortgage prediction model can provide transparent and actionable insights to borrowers, increase awareness about potential financial implications, and ensure reliability and fairness in predicting high-priced mortgages.

##Arij
### Metrics: Metrics should be chosen to reflect potential real- world impacts of the model.

* Model performance measures: What measures of model perfor- mance are being reported, and why were they selected over other measures of model performance?
  
**Accuracy:** The proportion of correct predictions. It is a common and straightforward measure, particularly for balanced datasets.

**Precision:** The ability of the model to correctly identify positive cases. It focuses on minimizing false positives.

**Recall (Sensitivity or True Positive Rate):** The ability of the model to correctly capture all positive cases. It emphasizes minimizing false negatives.

**F1 Score:** The harmonic mean of precision and recall, providing a balanced measure that considers both false positives and false negatives.

**Area Under the ROC Curve (AUC-ROC):** The performance of the model across various thresholds, providing a measure of the trade-off between true positive rate and false positive rate.

* Decision thresholds: If decision thresholds are used, what are they, and why were those decision thresholds chosen?

* Variation approaches:  How are the mea- surements and estimations of these metrics calculated? For ex- ample, this may include standard deviation, variance, confidence intervals, or KL divergence. Details of how these values are ap- proximated should also be included (e.g., average of 5 runs, 10-fold cross-validation). 

##Kerry
### Training Data

* The source of training data was the Home Mortgage Disclosure Act (HMDA) data.   
* The training and test data data was provided to us already spliced into training and test data for educational instructional purposes. 
* The provided training and test datasets contained 160338 rows and 23 columns together.  
* Define the meaning of all training data columns.  
* Define the meaning of all engineered columns.  
* State details of the distribution over various factors in the training datasets.

##Agnes
### Evaluation Data: Details on the dataset(s) used for the quantitative analyses in the card.

* Datasets used to evaluate the model:
  * [hmda_train_preprocessed.zip](https://github.com/arijlodhi/RML_Group3/blob/main/hmda_train_preprocessed.zip)
  * [hmda_test_preprocessed.zip](https://github.com/arijlodhi/RML_Group3/blob/main/hmda_test_preprocessed.zip)
* Motivation: Why were these datasets chosen? 
* Preprocessing: How was the data preprocessed for evaluation (e.g., tokenization of sentences, cropping of images, any filtering such as dropping images without faces)? 
* State the source of evaluation (or test) data 
* State the number of rows in evaluation (or test) data 
* State any differences in columns between training and evaluation (or test) data

##Arij
###  Quantitative Analysis: Quantitative analyses should provide the results of evaluating the model according to the chosen metrics, providing confidence interval values when possible. 

* State the metrics used to evaluate your group’s best remediated model

**Accuracy:** 0.9013
**Precision:** 0.6032	
**Recall:** 0.0159
**F1 Score:** 0.0310
**Area Under the ROC Curve (AUC-ROC):** 0.8200

* State the values of the metrics for training, validation, and evaluation (or test) data – evaluation (or test) metrics come from the most recent class full evaluation results, link under Assignment 1.

**ACC**	0.895
**AUC**	0.818
**F1**	0.404
**LOGLOSS**	0.273
**MSE**	0.082

* Unitary results: How did the model perform with respect to each factor?
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

## Kerry
### Ethical Considerations

* Describe potential negative impacts of using your group’s best remediated model:
* Consider math or software problems
* Consider real-world risks: who, what, when and how?
* Describe potential uncertainties relating to the impacts of using your group’s best remediated model:
* Consider math or software problems
* Consider real-world risks: who, what, when and how?
* Describe any unexpected or results encountered during training

##Agnes
### Caveats and Recommendations

This section should list additional concerns that were not covered in the previous sections. For example, did the results suggest any further testing? Were there any relevant groups that were no represented in the evaluation dataset? Are there additional recom- mendations for model use? What are the ideal characteristics of an evaluation dataset for this model?


## Collaboration
During the project, we fostered a collaborative environment and utilized effective communication channels to ensure smooth collaboration. We primarily communicated through regular team meetings, both in-person and online, where we discussed project progress, shared updates, and addressed any issues or concerns. Additionally, we maintained open communication channels through instant messaging platforms and email for day-to-day interactions.

To divide tasks, we initially assessed each team member's strengths, interests, and areas of expertise. Based on this assessment, we allocated tasks accordingly, considering the individual's skills and workload balance. We aimed for a fair distribution of responsibilities and ensured that each team member had the opportunity to contribute and develop their skills.

In terms of conflict resolution, we encouraged open and respectful discussions when disagreements arose. We actively listened to each other's perspectives, sought common ground, and worked towards finding mutually agreeable solutions. In case of significant conflicts, we sought the guidance of our project advisor or faculty member to help mediate and provide guidance for resolution.

Overall, our collaborative approach, effective communication, task allocation, and conflict resolution strategies allowed us to work efficiently as a team, leverage our collective strengths, and successfully complete the project.
