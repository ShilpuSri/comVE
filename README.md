# Commonsense-Validation-Explanation
This repository contains code for the NLP task Commonsense Validation and Explaination which was a part of CodaLab SemEval 2020 competetion: https://competitions.codalab.org/competitions/21080 
The task is to directly test whether a system can differentiate natural language statements that make sense from those that do not make sense. We worked on three subtasks:
The first task is to choose from two natural language statements with similar wordings which one makes sense and which one does not make sense; 
The second task is to find the key reason from three options why a given statement does not make sense; 
The third task asks machine to generate the reasons and we use BLEU to evaluate them.

The folder ALLData contains the entire dataset (training, dev and test set for all three subtasks)

The folder src/Kaggle_notebooks: contains notebooks for all the subtasks. These are Kaggle notebooks as we used GPU for faster modeling of data.

Subtask1 : We used 2 approaches:
(i) Using Google's Universal Sentence Encoder (USE-Lite)
(ii) Using BERT
Subtask2: Using BERT
Subtask3: GPT2 fine tuning and BLEU score evaluation - (GPT2-124M)

The folder evaluationtools_results contains all the scorer.py files, accuracy and BLEU score obtained and final output CSV files with outputs obtained.

Summary of Results:
Subtask A: Accuracy: USE-Lite - 78.3%
Subtask A: Accuracy: BERT - 88.0%
Subtask B: Accuracy: BERT: 83.1%
Subtask C: BLEU: 5.2967

For subtask C, we could get better results if we train on larger GPT2 model(e.g 345M parameters), but we used 124M as that was the max the laptop could support without running into memory issues.
