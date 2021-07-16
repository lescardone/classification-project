## DataFrames
- **df**: original DF

PREPROCESSED
- **df_cont**: DF with continuous variable columns only
- **df_cat**: DF with categorical variables only

PROCESSED
- **cat_dummies**: dummified categorical variables
- **df_cat_select**: 3 dummified categorical variables
- **impute_df**: DF of 35 features, with KNN feature imputation

COMBINE
- **df_all**: DF of 36 continuous and 3 categorical + target

## Feature Lists
- continuous_features
- categorical_features

For first pass model
- feature_list

For KNN NAN imputation
- correlated_features (continuous features)
    - na_features
    - notnull_features
- cat_correlated_features (categorical features)

## Functions
# Narrow Down Number Features
**percent_na_df(df, feature_list)**:   
HELPER FUNCTION
pass in DF and a list of features (continuous_features)
returns DF; ['features','percent_na']


**select_correlated(df)**:
pass in DF (df_cont)
narrows down amount of features (continuous)
selects 
    high correlated, 
    low NAN features
returns DF; ['features','percent_na',diabetes_mellitus']


**correlated_features(df)**:  
pass in DF (df_cont)
returns the continuous features from above in a list


# Split Feature List into HAS NAN and NONULLS
**na_feature_list(df, feature_list)**:
pass in DF and feature list (correlated features)

returns the features from our correlated features above that have NAN, in a list

**no_nulls_features(df, feature_list)**:
pass in DF and feature list (all continuous features)

returns the features that do NOT contain any NAN, in a list


# 36 Features
    ethnicity  
    gender  
    hospital_admit_source
    icu_admit_source  
    icu_stay_type  
    icu_type   
    d1_sysbp_max  
    d1_diasbp_min  
    d1_sysbp_noninvasive_max  
    d1_diasbp_noninvasive_min  
    weight  
    bmi   
    age  
    h1_sysbp_max  
    h1_diasbp_min  
    h1_diasbp_max  
    d1_glucose_min  
    d1_glucose_max  
    h1_sysbp_noninvasive_max  
    h1_diasbp_noninvasive_min  
    h1_diasbp_noninvasive_max  
    d1_potassium_min  
    d1_potassium_max  
    d1_creatinine_min  
    d1_creatinine_max  
    d1_sodium_min  
    d1_bun_min  
    d1_bun_max  
    glucose_apache
    d1_hematocrit_max  
    d1_hematocrit_min  
    d1_hemaglobin_min  
    d1_hemaglobin_max  
    d1_calcium_max  
    d1_hco3_min  
    sodium_apache  
    creatinine_apache  
    bun_apache  
    hematocrit_apache  
    h1_glucose_min  
    h1_glucose_max  
    arf_apache  