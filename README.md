# Deep-LLMADEminer
Deep-LLMADEminer Codebase for SMM4H 2024 Task 1 ADE extraction task

# Instructions on how to run the code

**Study name**: Deep-LLMADEminer: A deep learning and LLM pharmacovigilance pipeline for extraction and normalization of adverse drug event mentions on Twitter using SMM4H-2024 datasets

**Note:** There are three code files, representing **three** tasks in this specific study. Each task was implemented via **Google Colab**, thus input and output files should be placed in certain locations and/or folders in the **Google Drive** (Except for Task 2).

## Task 1: ADE Classification

- **<u>Required packages</u>**: ```transformers, nltk, torch, sklearn, tqdm, logging ```
- **Directory of training data** (original tweets): ```/content/drive/MyDrive/SMM4H-Task1/Train_2024/tweets.tsv```(original data directory, this data should include ```Tweet ID``` and their original tweet)
- **Directory of training data** (tweets with annotations): ```/content/drive/MyDrive/SMM4H-Task1/Train_2024/gold_annotations_complete.tsv```
- **Directory of validation data** (original tweets): ```/content/drive/MyDrive/SMM4H-Task1/Dev_2024/tweets.tsv```
- **Directory of validation data** (tweets with annotations): ```/content/drive/MyDrive/SMM4H-Task1/Dev_2024/gold_annotations_complete.tsv```
- **Directory of testing data**: ```/content/drive/MyDrive/SMM4H-Task1/tweets.tsv```
- **Prediction results should be at:** ```/content/prediction_data_results.csv```
- **Prediction results with original tweets merged**: ```/content/prediction_data_results_withtweet.csv```

## Task 2: ADE Span Extraction

- **<u>Required packages</u>**: ```os, time, openai```
- Directory: Default directory
- **Results from task 1 (tweets with ADEs)**:```prediction_data_results_withtweet task 1.csv```
- **Test tweets**: ```test_tweets.tsv```

## Task 3: ADE Normalization

- <u>**Required packages**</u>: ```transformers, torch, sklearn, joblib```
- **Directory of training data** (original tweets): ```/content/drive/MyDrive/LHS 712_Group_Task1/SMM4H-Task1/Train_2024/tweets.tsv```
- **Directory of training data** (tweets with annotations): ```/content/drive/MyDrive/LHS 712_Group_Task1/SMM4H-Task1/Train_2024/gold_annotations_complete.tsv```
- **Directory of validation data** (original tweets): ```/content/drive/MyDrive/LHS 712_Group_Task1/SMM4H-Task1/Dev_2024/tweets.tsv```
- **Directory of validation data** (tweets with annotations, including **text spans**): ```/content/drive/MyDrive/LHS 712_Group_Task1/SMM4H-Task1/Dev_2024/gold_annotations_complete.tsv```
- **Directory of validation data** (tweets with annotations, including MedDRA ID): ```/content/drive/MyDrive/LHS 712_Group_Task1/SMM4H-Task1/Dev_2024/gold_annotations_for_evaluation.tsv```
- **Sample submission form**: ```/content/drive/MyDrive/LHS 712_Group_Task1/SMM4H-Task1/Sample_submissions/sample_submission.tsv```
- **All the unique preferred terms IDs from the training set**: ```/content/drive/MyDrive/LHS 712_Group_Task1/SMM4H-Task1/Dev_2024/seen_concepts.txt```
- **MedDRA ID**: ```/content/drive/MyDrive/LHS 712_Group_Task1/SMM4H-Task1/Resource/llt.asc```
- **External data for prediction**: ``/content/drive/MyDrive/LHS 712_Group_Task1/SMM4H-Task1/GPT_results_for_ADRtext_1by1_new.csv``
