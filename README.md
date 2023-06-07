# RML_Group3
## **Group Assignments for Responsible Machine Learning**

### **Group assignment 1 - Machine Learning Model Training**

The **assignment 1** statement requests training at least two explainable models while ensuring best practices such as reproducibility, validation-based early stopping, and grid search are used.

For our **assignment 1**, we decided to train five explainable models: EBM, GAM, GLM, XGB, and tree, using the PiML package. For reproducibility, we set the seed to SEED = 12345.

**This portfolio provides the following content for assignment 1:**

1. [hmda_train_preprocessed.zip](https://github.com/arijlodhi/RML_Group3/blob/main/hmda_train_preprocessed.zip): This file was used as training data to train the models. Users can download it.
2. [hmda_test_preprocessed.zip](https://github.com/arijlodhi/RML_Group3/blob/main/hmda_test_preprocessed.zip): This file was used as test data to retrieve test data scores. Users can download it.
3.  [Group_3_Assignment_1.ipynb](https://github.com/arijlodhi/RML_Group3/blob/main/Group_3_Assignment_1.ipynb): This file is the code file for the project. Users can view and run the code through Jupyter Notebook.
4. [Download test data score CSV file for EBM](https://github.com/arijlodhi/RML_Group3/blob/main/group3_piml_EBM.csv): This file is the test data score CSV file that was extracted from the Jupyter Notebook file after training the EBM model using PiML. Users can download it.
5. [Download test data score CSV file for GAM](https://github.com/arijlodhi/RML_Group3/blob/main/group3_piml_GAM.csv): This file is the test data score CSV file that was extracted from the Jupyter Notebook file after training the GAM model using PiML. Users can download it.
6. [Download test data score CSV file for GLM](https://github.com/arijlodhi/RML_Group3/blob/main/group3_piml_GLM.csv): This file is the test data score CSV file that was extracted from the Jupyter Notebook file after training the GLM model using PiML. Users can download it.
7. [Download test data score CSV file for XGB](https://github.com/arijlodhi/RML_Group3/blob/main/group3_piml_XGB.csv): This file is the test data score CSV file that was extracted from the Jupyter Notebook file after training the XGB model using PiML. Users can download it.
8. [Download test data score CSV file for tree](https://github.com/arijlodhi/RML_Group3/blob/main/group3_piml_tree.csv): This file is the test data score CSV file that was extracted from the Jupyter Notebook file after training the tree model using PiML. Users can download it.

### **Group assignment 2 - Machine Learning Model Analysis**


The instructions below will guide you through the process.

**Objective**

The objective of this assignment 2 is to analyze and evaluate the ML models developed in Assignment 1. We assessed the explanatory results of the models EBM, GLM, and XGB from both a domain knowledge perspective and by comparing the differences between the models. Additionally, we calculated global feature importance using regression coefficients, Shapley values, or other reputable techniques.

**Instructions**

For each section below, our goal is to evaluate the explanatory results and assess their coherence with domain knowledge. Pay attention to the logical and informative differences between the models.

1. **Global Feature Importance:**
   - Utilize regression coefficients, Shapley values, or other reputable techniques to calculate global feature importance for your models.

2. **Local Feature Importance:**
   - Using similar approaches to those in Section 1, calculate local feature importance for your models at three percentiles of predicted probability.

3. **Partial Dependence:**
   - The provided template calculates partial dependence for each main effect feature of each model, enabling the analysis of feature behavior under each model.

## Conclusion

By following the instructions and conducting a thorough analysis of the ML models from Assignment 1, you will gain insights into their explanatory power, compare the models' differences, and calculate feature importance. This analysis will enable you to understand the behavior of the models and their performance in predicting the target variable.

Happy analyzing!

**This portfolio provides the following content for assignment 2:**

1. [hmda_train_preprocessed.zip](https://github.com/arijlodhi/RML_Group3/blob/main/hmda_train_preprocessed.zip): This file was used as training data to train the models. Users can download it.
2. [Plot partial dependence for the most important features and models](https://github.com/arijlodhi/RML_Group3/blob/main/RML_assignment2.pdf): This PDF file contains images illustrating the partial dependence plots for the most important features and models.


## Assignment 1 contributors
Team members: **Agnes Nguenda, Arij Ahmed Khan Lodhi , Bagya Widanagamage**

## Assignment 2 contributors
Team members: **Agnes Nguenda, Arij Ahmed Khan Lodhi , Kerry McKeever**

## Collaboration
During the project, we fostered a collaborative environment and utilized effective communication channels to ensure smooth collaboration. We primarily communicated through regular team meetings, both in-person and online, where we discussed project progress, shared updates, and addressed any issues or concerns. Additionally, we maintained open communication channels through instant messaging platforms and email for day-to-day interactions.

To divide tasks, we initially assessed each team member's strengths, interests, and areas of expertise. Based on this assessment, we allocated tasks accordingly, considering the individual's skills and workload balance. We aimed for a fair distribution of responsibilities and ensured that each team member had the opportunity to contribute and develop their skills.

In terms of conflict resolution, we encouraged open and respectful discussions when disagreements arose. We actively listened to each other's perspectives, sought common ground, and worked towards finding mutually agreeable solutions. In case of significant conflicts, we sought the guidance of our project advisor or faculty member to help mediate and provide guidance for resolution.

Overall, our collaborative approach, effective communication, task allocation, and conflict resolution strategies allowed us to work efficiently as a team, leverage our collective strengths, and successfully complete the project.
