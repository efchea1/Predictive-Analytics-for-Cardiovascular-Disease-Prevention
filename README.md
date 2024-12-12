# Predictive-Analytics-for-Cardiovascular-Disease-Prevention
Utilizing the BRFSS 2021 dataset, this project employs machine learning models to predict cardiovascular disease risk. Techniques include Logistic Regression, Decision Trees, KNN, and Random Forest, evaluated by AUC and Brier scores to enhance CVD prevention.

### Project Background: 

Prediction of Cardiovascular Disease Risk Using Machine Learning

### Introduction: 

Cardiovascular disease (CVD) continues to be a leading cause of death globally, necessitating advanced strategies to predict and mitigate risk factors. This project aims to harness machine learning technologies to identify individuals at increased risk of cardiovascular diseases using data from the 2021 Behavioral Risk Factor Surveillance System (BRFSS). By deploying various predictive models, this initiative seeks to enhance the precision of preventive healthcare interventions, making a significant step towards personalized medicine.

### Data Source: 

The dataset employed in this project is obtained from the 2021 BRFSS, which compiles extensive information on health-related behaviors, chronic health conditions, and preventive service usage among U.S. adults. The dataset includes 308,854 participants and features 304 unique variables, but this study focuses on 19 variables directly related to lifestyle factors influencing CVD risk.

### Selected Variables:

**Outcome Variable:** *Heart Disease* (binary: "Yes", "No")

**Predictors:** A combination of numerical and categorical variables relevant to CVD risk such as Height, Weight, BMI, Alcohol Consumption, and various health and lifestyle indicators.
Preprocessing Steps: The data was meticulously prepared through several preprocessing steps:

### Renaming columns for consistency.

Converting categorical data into factors for proper analysis.
Scaling numerical variables to normalize data.
Imputing missing values using the mean for numerical variables and the mode for categorical variables.
Splitting the dataset into training (75%) and testing (25%) sets to validate the models effectively.
Methodology: A variety of machine learning models were explored to predict the risk of CVD:

Logistic Regression serves as a baseline model.
Decision Tree offers transparent decision-making insights.
K-Nearest Neighbors (KNN) provides predictions based on local similarity.
Random Forest captures complex patterns through ensemble learning.
Each model was rigorously trained and tested, with performance evaluated primarily using the Area Under the ROC Curve (AUC) and other metrics like Brier scores for probability accuracy.

Objective: The primary objective is to utilize predictive analytics to facilitate the early identification of high-risk individuals for targeted preventive measures, thus reducing the overall incidence and burden of cardiovascular diseases. Through this project, we aim to integrate data-driven insights into healthcare strategies, enhancing the efficiency and effectiveness of CVD prevention efforts.

# Report - Study Findings

### Introduction:

Cardiovascular disease (CVD) remains a leading cause of mortality globally, urging the need for effective preventive strategies. This project leverages predictive analytics to identify individuals at heightened risk of CVD using the 2021 Behavioral Risk Factor Surveillance System (BRFSS) data. By developing machine learning models capable of discerning patterns and risk factors in patient data, this initiative aims to enhance preventive intervention targeting, ultimately reducing the incidence and burden of heart disease. This approach promises to improve the precision of preventive healthcare, aligning with current trends toward personalized medicine.

### Data:

The data for this project is sourced from the 2021 Behavioral Risk Factor Surveillance System (BRFSS), hosted on Kaggle. This extensive dataset provides a comprehensive view of health-related behaviors, chronic health conditions, and the use of preventive services among U.S. residents. It includes 308,854 observations with 304 unique variables, focusing on various aspects that could influence cardiovascular disease (CVD) risk.

For this project, 19 variables were specifically selected due to their relevance to lifestyle factors associated with CVD risk. These include both numerical and categorical variables:
Outcomes: The primary outcome variable for this project will be Heart Disease, a binary variable (“Yes”, “No”) indicating the presence or absence of heart disease. This outcome will allow for the development of binary classification models.
Predictors: The predictors will include a mix of numerical and categorical variables:
Numerical: Height (cm), Weight (kg), Body Mass Index (BMI), Alcohol Consumption, Fruit Consumption, Green Vegetables Consumption, Fried Potato Consumption.
Categorical: General Health, Checkup Frequency, Exercise Regularity, Depression Status, Diabetes Status, Arthritis Presence, Sex, Age Category, Smoking History, Skin Cancer, and Other Cancer.

### Pre-preprocessing Steps:

The raw data underwent several preprocessing steps to prepare for analysis. These preprocessing steps transformed the dataset into a clean, well-formatted, and analysis-ready format. The structured approach to data handling helps reduce variability and bias in the predictive models, thus enhancing the reliability of the outcomes derived from this dataset.

Renaming Columns: Columns such as 'Weight_(kg)' and 'Height_(cm)' were renamed to 'Weight_kg' and 'Height_cm' for consistency and easier handling in R.
Data Splitting: The dataset was divided into training (75%) and testing (25%) sets using the initial_split function to ensure that models are trained on a large subset of the data and tested on an entirely separate set for unbiased evaluation.

Factor Conversion: Categorical variables were converted to factors to properly reflect their nature in the statistical models. This step ensures that algorithms interpret these variables correctly.
Scaling: Numerical variables were scaled to have zero mean and unit variance. This normalization is crucial for models like logistic regression and KNN, which are sensitive to the scale of input data.
Handling Missing Values: Missing values were imputed using the mean for numerical variables and the mode for categorical variables to maintain consistency and avoid introducing bias by removing missing data.

### Methods:

For the "Predictive Analytics for Cardiovascular Disease Prevention" project, various machine learning models were utilized to develop robust predictive systems. The selected models include Logistic Regression, Decision Tree, K-Nearest Neighbors (KNN), and Random Forest. Each model was fitted using a training dataset and evaluated against a testing dataset to ensure the reliability of predictions.

### Models and Fitting:

**Logistic Regression:** This model serves as the baseline, providing a benchmark for comparing more complex models due to its interpretability and efficiency in binary classification tasks. It was implemented using the glm function in R with a binomial family, indicative of its classification purpose.

**Decision Tree:** Decision trees were utilized to provide a transparent model that illustrates the decision rules directly derived from the data. It was implemented using the rpart package, favored for its simplicity and interpretability.

**K-Nearest Neighbors (KNN):** This non-parametric method relies on the nearest data points for prediction, offering insights into local data structures and feature relationships. It was implemented using the kknn package, which is suited for handling classification tasks with a distance-based approach.

**Random Forest:** As an ensemble method, Random Forest was chosen for its strength in capturing complex non-linear relationships and its robustness against overfitting. The ranger package was used due to its efficient handling of large datasets and capability to generate probability estimates.

### Evaluation Metrics:

* Area Under the Curve (AUC): The primary metric used to evaluate each model, AUC measures the ability of the model to discriminate between the classes effectively. Higher AUC values indicate better model performance.

* Receiver Operating Characteristic (ROC) Curve: This was computed for each model to assess its discriminative ability. The ROC curve is a graphical plot that illustrates the diagnostic ability of a binary classifier system as its discrimination threshold is varied.

* Brier Score: Used for some models to measure the accuracy of probabilistic predictions. It quantifies the mean squared difference between predicted probabilities and the actual outcomes.

### Model Comparison:

The model comparison based on AUC, along with considerations for computational efficiency and interpretability, guides the selection of the most appropriate model(s) for deployment in practical scenarios within cardiovascular disease prevention. This thorough evaluation ensures that the models perform well statistically and align with clinical and practical requirements for predicting cardiovascular disease risk. Each model's performance was rigorously compared using the AUC metric derived from the ROC curve. This comparison is crucial to understanding which model performs best in terms of sensitivity (true positive rate) and specificity (false positive rate). Logistic Regression often provides a good balance between complexity and performance, making it a strong candidate for further tuning and operational use. Decision Trees provide a clear understanding of the decision-making process but often at the cost of lower complexity and potentially lower performance. KNN's performance is dependent on the choice of 'k' and the distance metric, which might require adjustments based on the dataset characteristics. Random Forest typically shows high performance on complex datasets with numerous features but may require extensive computational resources.

### Results:

Table 1 shows the descriptive statistics of the study. The dataset includes 308,854 records, detailing health-related variables for cardiovascular disease risk analysis. The majority of participants report Very Good (36%) or Good (31%) health, with regular annual checkups reported by 78% and a similar percentage engaging in regular exercise. Chronic conditions are prevalent, with 8.1% having heart disease and approximately 9.7% diagnosed with skin or other cancers. Depression impacts 20% of the population, diabetes affects 13%, with an additional 2.2% indicating pre-diabetes, and arthritis is reported by 33%. Demographically, there is a slight female majority (52%), with the most represented age groups being 65-69 (11%) and 60-64 (10%). Average physical measures are a height of 171 cm (SD = 11), a weight of 84 kg (SD = 21), and a BMI of 29 (SD = 7). Lifestyle data shows that 41% of the sample has a history of smoking, with an average alcohol consumption of 5 units (SD = 8). Dietary intake reflects average consumption of fruits and vegetables with minimal fried potato intake.

### Model Performance Overview:

**Logistic Regression:** The Logistic Regression model achieved an AUC of 0.837 and a Brier score of 0.063, indicating a strong ability to differentiate between the positive and negative classes. This performance is commendable, reflecting the model’s efficiency in handling binary classification with a balance of sensitivity and specificity. The model's interpretability also allows for easy extraction and understanding of the influence of each predictor on the likelihood of CVD, making it a valuable tool for clinical decision support. 

**Decision Tree:** The Decision Tree model exhibited an AUC of 0.768 and a Brier score of 0.074. While AUC is lower and the Brier score is higher than that of Logistic Regression, this result still suggests a fair discriminatory ability. Decision Trees provide a graphical representation of decision-making processes, which can be particularly useful for clinical explanations but might lack the robustness provided by more complex models. 

**K-Nearest Neighbors (KNN):** The KNN model, particularly challenging to optimize due to its dependency on the choice of neighbors and distance metric, recorded an AUC of 0.674 and a Brier score of 0.097. This lower performance highlights its sensitivity to the local data structure and possibly the imbalances within the dataset, which can affect its generalizability and reliability in clinical settings. 

**Random Forest:** Achieving an AUC of 0.824 and a Brier score of 0.065, the Random Forest model demonstrated strong performance, slightly underperforming compared to Logistic Regression but still robust. Its strength lies in handling high-dimensional data and capturing complex, non-linear interactions between features, which are critical in medical datasets characterized by intricate biological interactions. 

### Comparative Analysis: 

**Sensitivity and Specificity:** The ROC curves revealed that Logistic Regression and Random Forest achieved a more favorable balance between sensitivity (true positive rate) and specificity (false positive rate), essential for minimizing both false negatives and false positives in clinical applications. 

**Calibration:** In terms of calibration, Logistic Regression showed probabilities that closely matched the actual observed outcomes, suggesting that its predictions are both accurate and reliable. Random Forest and Decision Tree models, while slightly less calibrated, offered insights into risk factors with complex interactions. 

**Computational Efficiency:** Logistic Regression provided a significant advantage in terms of computational efficiency, making it suitable for scenarios where quick model training and prediction are necessary. Random Forest, although computationally more intensive, justified its use through enhanced predictive accuracy for complex cases. Logistic Regression emerged as the most effective model for this application, given its high AUC, low Brier score, excellent calibration, and ease of interpretation. These characteristics make it particularly suitable for deployment in a clinical setting where understanding and trust in the model’s predictions are crucial. Meanwhile, Random Forest remains a valuable alternative for scenarios where capturing more complex patterns in data can provide additional insights into patient risk profiles.

### Discussion:

The analysis conducted in the predictive modeling of cardiovascular disease (CVD) risk, while comprehensive, presents several limitations that warrant consideration. First, the reliance on the Behavioral Risk Factor Surveillance System (BRFSS) dataset, primarily a telephone survey, introduces potential biases such as self-reporting inaccuracies and non-response bias. These factors could affect the reliability of the input data, especially concerning lifestyle and health status variables, potentially skewing the predictive accuracy of the models.

Another limitation is the imbalance in the dataset regarding the outcome variable—heart disease prevalence. With only 8.1% of the samples representing positive cases, there's a risk that models, especially those like K-Nearest Neighbors (KNN), could be biased towards predicting the majority class, reducing sensitivity to detect actual disease cases. This imbalance was somewhat mitigated in models like Logistic Regression and Random Forest through internal mechanisms such as threshold moving and ensemble strategies, but it remains a concern for model generalizability to other populations or datasets.

From a methodological standpoint, while the chosen metrics (AUC, Brier score, calibration) are appropriate for binary classification tasks, relying solely on these might overlook other aspects like precision-recall trade-offs, which are critical in clinical settings where the cost of false negatives is high. Future analyses could benefit from incorporating additional performance metrics such as the F1 score or the use of precision-recall curves, especially in the context of imbalanced datasets.

Alternative approaches could involve more sophisticated resampling techniques or synthetic data generation methods such as the Synthetic Minority Oversampling Technique (SMOTE) to address class imbalance. Additionally, employing advanced model calibration techniques or exploring different ensemble methods could further enhance model performance and interpretability. Exploring models designed for imbalanced data, like cost-sensitive learning algorithms, could also provide new insights and potentially improved predictive performance.
