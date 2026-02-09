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
└── metrics_tables/
    ├── balanced_metrics_table.png
    ├── nonstratified_metrics_table.png
    ├── stratified_metrics_table
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
