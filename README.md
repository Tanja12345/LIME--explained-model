# LIME--explained-model
Use SVM to classify content  as atheism or Christian. And using LIME to explain the prediction.

## A result of an individual data
<img width="544" height="217" alt="image" src="https://github.com/user-attachments/assets/d5e7b953-3dc1-4e62-ac1f-3dd4faf1e85b" />

## Data processing
1. Data loading
   load data from fetch_20newsgroup
2. Vectorized
   using TFidVectorizer to vectorize content into sparse matrices
   using training data to fit the vectorizer and using this vectorizer to transform training data into training matrices
   using the vetorizer to transform the test data into test matrices

## Model training
1. Prepare a learner of SVM with kernel 'rbf'
 1. Fit the learner using training matrices and their targets
 2. Using fitted model to predict the test matrices

## Model prediction
Calculate accuracy

## Pipeline
prepare pipeline for LIME
1. Put Vectorized and Model training into a pipeline
2. Using this pipeline for a single original data and calculate its prediction probability (every classification's prediction probability)

## Using LIME to explain one prediction
1. Prepare a LIME model with accorded categories of classification
2. choosing an index for explaining and the number of features want to be showed
3. Using 'explain_instance' to generates explanations for a prediction and save the result

For the result, we can use:
1. 'as_list()' to digitally see every features' coefficients
2. 'as_pyplot_figure()' or 'show_in_notebook()' to tabular display 
   
 
 
