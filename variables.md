## DataFrames
- **df**: original DF
- **df_cont**: DF with continuous variable columns only

- **df_cat**: DF with categorical variables only
- **cat_dummies**: dummified categorical variables

## Feature Lists
- continuous_features
- categorical_features

## Functions  
**percent_na_df(df, feature_list)**:   
pass in df and a list of features
returns DF; ['features','percent_na']


**select_correlated(df)**:  
returns DF; ['features','percent_na',diabetes_mellitus']


**correlated_features(df)**:  
returns the features from above in a list


**na_feature_list(df, feature_list)**:
pass in df and correlated feature list

returns the features from our correlated features above that have NAN, in a list

**no_nulls_features(df, feature_list)**:
pass in df and a list of all features

returns the features that do not contain any NAN, in a list

