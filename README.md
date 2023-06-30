# RML_Group3 Model Card
## **Final Project for Responsible Machine Learning**


### Model Details: Basic information about the model.

The model's purpose is to identify mortgages that have significantly higher APRs compared to the market estimate. The model aims to provide transparency by flagging mortgages that may impose higher costs on borrowers. By predicting high-priced mortgages, the model can contribute to increasing awareness and understanding of the potential financial implications for borrowers.

* Contributors:<br>
**Agnes Nguenda**, agnesdanielleflore.nguenda@gwmail.gwu.edu <br>
**Arij Ahmed Khan Lodhi**, arijahmedkhan.lodhi@gwu.edu <br> 
**Kerry McKeever**, kerry.mckeever@gwu.edu <br>

#Arij
* Model date: July 2023
* Model version: 1.0
* State the software used to implement your group’s best remediated model
* State the version of the modeling software for your group’s best remediated model
* Model type: State the type of your group’s best remediated model
* Information about training algorithms, parameters, fairness constraints or other applied approaches, and features
  * State the columns used as inputs in your group’s best remediated model
  * State the columns used as targets in your group’s best remediated model
  * State the hyperparameters or other settings of your group’s best remediated model
* Paper or other resource for more information
* Citation details

* MIT License

Copyright (c) 2023

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### Comments or questions regarding this model can be forwarded to (insert emai), (Insert email), and @kerry.mckeever@gwu.edu. 

##Kerry 
### Intended Use:  Use cases that were envisioned during development.

* The business value of our best produced model is to ensure an unbiased and reliable method to decide whether mortgages should be granted to different housing applicants. This both benefits the consumers, who are able to purchase houses, as well as lenders, who are ensuring they are choosing patrons who will pay back their loans in a timely manner and be an add value to the company.

* The best produced model (EBM) should be used when there is ample applicant information, including but not limited to: debt to income ratio, loan amount, loan to value ratio, property value, income, and demographic information. 

* Our intended users for this model are people with all demographic backgrounds, as out model accounts for these differences and the biases that may be associated with them in previous loan models.  (should we add cut offs for incomes/ ages? Ie: The intended user for this model receives an income of over ___ and is over ___ in age?) 

* No further uses for this model are currently known.  

##Agnes
### Factors: include demographic or phenotypic groups, environmental conditions, technical attributes, or others

* Relevant factors: What are foreseeable salient factors for which model performance may vary, and how were these determined?
* Evaluation factors: Which factors are being reported, and why were these chosen? If the relevant factors and evaluation factors are different, why?

##Arij
### Metrics: Metrics should be chosen to reflect potential real- world impacts of the model.

* Model performance measures: What measures of model perfor- mance are being reported, and why were they selected over other measures of model performance? 
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

* Datasets: What datasets were used to evaluate the model? 
* Motivation: Why were these datasets chosen? 
* Preprocessing: How was the data preprocessed for evaluation (e.g., tokenization of sentences, cropping of images, any filtering such as dropping images without faces)? 
* State the source of evaluation (or test) data 
* State the number of rows in evaluation (or test) data 
* State any differences in columns between training and evaluation (or test) data

##Arij
###  Quantitative Analysis: Quantitative analyses should provide the results of evaluating the model according to the chosen metrics, providing confidence interval values when possible. 

* State the metrics used to evaluate your group’s best remediated model
* State the values of the metrics for training, validation, and evaluation (or test) data – evaluation (or test) metrics come from the most recent class full evaluation results, link under Assignment 1.
* Unitary results: How did the model perform with respect to each factor?
* Intersectional results: How did the model perform with respect to the intersection of evaluated factors?
* Provide at least one plot or table from each weekly assignment for a total of at least six plots,
that must include the global variable importance and partial dependence of your group’s best
remediated model.
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
