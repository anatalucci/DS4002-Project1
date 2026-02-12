# Project 1 - Amazon Project Rating Analysis 
## Software 

Primary Software: Jupyter Notebook  
  
Add-on Packages: 
- counter (from collections) 
- pandas
- os 
- re
- numpy 
- tensorflow
- Tokenizer (from tensorflow.keras.preprocessing.text)
- pad_sequences (from tensorflow.keras.preprocessing.sequence)
- train_test_split (from sklearn.model_selection)
-  Model (from tensorflow.keras.models)
- Input, Embedding, Conv1D, GlobalMaxPooling1D, Dense, Dropout, Concatenate (from tensorflow.keras.layers) 
- plot_model (from tensorflow.keras.utils)
- confusion_matrix (from sklearn.metrics)
- matplotlib.pyplot 
- seaborn 
- accuracy_score, precision_score, recall_score, f1_score (from sklearn.metrics) 
- BinaryCrossentropy (from tensorflow.keras.losses)

Platform: macOS

## Documentation Map

```
Data/
├── data_origin.txt
├── filtered_firestick_reviews.csv
├── firestick_reviews_cleaned.csv
└── most_reviewed_asin.csv

Outputs/
├── EDA/
│   ├── average_star_rating_by_year.jpg
│   ├── distribution_of_ratings.jpg
│   ├── heatmap_of_reviews.jpg
│   ├── number_of_reviews_by_year.jpg
│   └── ratings_by_year.jpg
├── confusion_matrices/
│   ├── balanced_confusion_matrix.png
│   ├── nonstratified_confusion_matrix.png
│   └── stratified_confusion_matrix.png
├── metrics_tables/
    ├── balanced_metrics_table.png
    ├── nonstratified_metrics_table.png
    ├── stratified_metrics_table
    └── text_cnn_model.png
└── text_cnn_model.png

Scripts/
├── EDA.ipynb
├── cleaned_data.ipynb
├── data_analysis_and_evaluation.ipynb
└── initial_cleaning.ipynb

.gitignore
License
README.md
```

## Instructions
#### Pre-Cleaning  
- Download the required packages
#### Cleaning  
1. Upload the dataset most_reviewed_asin.csv  
2. Remove rows where verified purchase is false  
3. Drop columns "images", "parent_asin", "user_id", and "helpful_vote"
4. Edit the column "timestamp" to only display year  
5. Save to a new csv (firestick_reviews_cleaned.csv)
#### EDA  
1. Upload the dataset firestick_reviews_cleaned.csv
2. Create a graph of the distribution of stars and save as an image to the outputs folder on Github
4. Create a graph of the distribution of reviews by year and save as an image to the outputs folder on Github
5. Create a graph of the average star per year and save as an image to the outputs folder on Github
6. Create a graph of the number of stars per year and save as an image to the outputs folder on Github
7. Create a heatmap of the number of reviews per star by year and save as an image to the outputs folder on Github
#### Data Analysis  
1. Clean data to remove uppercase characters, non-word characters, extra whitespace
2. Remove reviews with 3-star reviews
3. Save to a new csv (filtered_firestick_reviews.csv)
4. Create a copy of the dataset and create binary labeling for the star-ratings (1 for 4-5 stars, 0 for 1-2 stars)
5. Save to new csv as a column
6. Create a data frame to combine the text in the columns "text" and "title"
7. Set the maximum words and maximum length based on the number of rows and length of text
8. Tokenize the text by replacing words that are not in the vocab and assign integers to words
9. Convert sequences of text into sequences of integers and pad the sequences to be the same length
10. Create two train splits: one with stratification and one without stratification  
11. Build the text CNN to classify the reviews  
    a. Set the size of each word vectors and define the input to be a sequence of integers with size maximum length  
    b. Create three convulations with different kernel sizes (3, 4, 5)  
    c. Create three pools to reducde the size of each input (based on each convolution)  
    d. Combine the pooled inputs, create a dropout layer to prevent overfitting and define outputs with sigmoid-activation to output predicted class  
    e. Define the model with binary cross-entropy loss, the adam optimizer, and accuracy metric  
    f. Save a visualization of the model as an image to outputs folder  
12. Train the model on the train split for 30 epochs (one for the stratified and one for the nonstratified)
13. Create two confusion matrices (one for stratified and one for nonstratified)  
    a. Save the plots as images to outputs folder
14. Create two metrics tables (one for stratified and one for nonstratified)  
    a. Report accuracy, precision, recall, f1, and binary cross-entropy  
    b. Save the two metrics tables as images to the outputs folder  
#### Mitigating the Class Imbalance  
1. Get the indices for each class
2. Ensure equal sizes of the classes and randomly sample an equal amount from each class (positive and negative)
3. Combine and shuffle the samples
4. Create a new set
5. Create a new train split with the balanced data
6. Clone and apply the model to the balanced split
7. Create a confusion matrix for the balanced data  
     a. Save the matrix as an image to outputs folder
8. Create a metric table for the balanced data, reporting same metrics  
     a. Save as an image to outputs folder 


## References 
[1] “Amazon Reviews’23,” amazon-reviews-2023.github.io. https://amazon-reviews-2023.github.io/  
[2] R. Nandagopal, A. Jayakumar, and G. Manokaran, “Impact of Online Reviews on Consumer Purchasing Decisions.” 

‌
‌

