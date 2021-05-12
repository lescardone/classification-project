# Classification Project: Predicting Diabetes Mellitus

## Question/Need:
*What is the framing question of your analysis, or the purpose of the model/system you plan to build?*
- How accurately can we predict Diabetes Mellitus given data collected during patients first 24 hours in the ICU?
- Which models provide the most accurate prediction?

*Who benefits from exploring this question or building this model/system?*

With hospital overwhelm across the United States during the COVID-19 pandmic, healthcare workers have struggled to treat an overwhleming amount of patients in critical condition. 

"Intensive Care Units (ICUs) often lack verified medical histories for incoming patients. A patient in distress or a patient who is brought in confused or unresponsive may not be able to provide information about chronic conditions such as heart disease, injuries, or diabetes. Medical records may take days to transfer, especially for a patient from another medical provider or system. Knowledge about chronic conditions such as diabetes can inform clinical decisions about patient care and ultimately improve patient outcomes." ([source](https://www.kaggle.com/c/widsdatathon2021/overview/description))

## Data Description:
*What dataset(s) do you plan to use, and how will you obtain the data?*  

This project, inspired by the Women in Data Science Datathon 2021 competition, focuses on the chronic condition of diabetes. The data has been provided by [MIT’s GOSSIS (Global Open Source Severity of Illness Score)](https://gossis.mit.edu/) initiative. (Other credits: [West Big Data Innovation Hub](https://westbigdatahub.org/) and [WiDS Datathon Committee](https://www.widsconference.org/committee-2021.html).)

There are 130,157 samples in the training data that I will break into a training, validation, and hold-out set.

*What is an individual sample/unit of analysis in this project? What characteristics/features do you expect to work with?*

There are 181 columns of features. 33% are labs, 29% are vitals, and 38% are categorized as other (includes demographic identifiers).

The target is binary for diabetes mellitus. Whether the patient has or has not been diagnosed with diabetes mellitus.

## Tools:
*How do you intend to meet the tools requirement of the project?*
- Impute missing values
- Feature engineering
- Rigorous model selection and evaluation (i.e. proper validation and testing)
- I will train and validate on KNN, Logistic Regression, Gradient Boosted Trees, Naive Bayes, and hopefully XGBoost.

I plan to spend most of my time evaluating different model types and tuning hyperparameters, rather than intense feature engineering.

*Are you planning in advance to need or use additional tools beyond those required?*
- No, not at the moment.

## MVP Goal:
*What would a minimum viable product (MVP) look like for this project?*
- Data cleaned (missing values, bad formatting, etc)
- Basic KNN and Logistic Regression Model
- Basic model evaluation metrics
