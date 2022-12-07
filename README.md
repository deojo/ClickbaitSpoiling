# SemEval 2023 Task 5: - Clickbait Spoiling

The problem is, ”SemEval 2023 - Clickbait Spoil- ing,” to generate spoilers for clickbait passages with a subtask of classifying what kind of spoiler is expected from a given article. The problem is a supervised question answering task with a subtask of supervised multiclass classification.
The subtask is then to classify the spoiler into one of ’phrase’, ’passage’, and ’multi’ so they are easier to generate. This subtask may help in generating spoilers but is not my focus for the project.

## Description

Clickbait lures users into clicking them and wasting. Generally, these articles cover frivolous topics, are unnecessarily long, and are inundated with ad- vertisements. Their headlines are often grossly misleading and provocative. Clickbait is a vehicle for socially damaging fake news and are a security risk because they can redirect to sites that phish for user data (Shu et al., 2018). But sometimes they can be interesting! Spoiling clickbait automatically avoids users having to open the articles and make themselves vulnerable.

## Getting Started

### Dependencies

The project has been developed and tested on Google Colab using Python 3.7 version. So it is recommended to have following prequisites installed on the system where this program will be executed:
   1. Python 3.7 version
   2. Jupyter Notebook
   3. After execution, the project will download all the necessary dependies required for its execution.

### Installing
   
   1 .Either clone the repo with git clone --recursive https://github.com/deojo/ClickbaitSpoiling.git or download the zip file from the repository and unzip the contents in a project folder.

   2. Make sure that the project folder contains: ProjectDJoshi_Final.ipynb, train.jsonl, validation.jsonl
   
   3. Execute all cells of ProjectDJoshi_Final.ipynb in Jupyter Notebook


### Program Parameters

The project is configured with default parameters for optimum output. For basic execution, no change is needed.


To override the default parameters, go to the 5th code cell titled 'Override above settings for best configuration' and follow the instructions as below:

    a: Document QA: modify the parameters defined in def set_qa_statement_configuration() on line# 26
        TOP_N_ROUGE_SCORES (default is 0) (All paragaphs are selected). Enter a positive integer (15  is average targetParagraph length) for selecting TOP N ROUGE score targetParagraphs
        QA_DROPOUT_HIDDEN (default is 0.2) to change BERT models "hidden_dropout_prob" parameter
        QA_DROPOUT_ATTENTION (default is 0.2) to change BERT models "attention_probs_dropout_prob" parameter
        QA_LEARNING_RATE (default is 3e-5) to change the learning rate for training
        QA_WEIGHT_DECAY (default is 0.01) to change weight decay for optimizer
        QA_EPOCH_MAX (default is 10) to change number of training epochs
        QA_MODELS (default 'roberta-base') to change underlying BERT model

    b: TargetParagraph Extraction : modify the parameters defined in def set_se_configuration() on line# 4
        SE_USE_CLASSWEIGHTS (default is 0 i.e no classweights) change to 1 to automatically select class weights based on the distribution in the training file.
        TOP_N_ROUGE_SCORES (default is 8) (All paragaphs are selected). Enter a positive integer (15  is average targetParagraph length) for selecting TOP N ROUGE score targetParagraphs
        SE_DROPOUT_HIDDEN (default is 0.1) to change BERT models "hidden_dropout_prob" parameter
        SE_DROPOUT_ATTENTION (default is 0.1) to change BERT models "attention_probs_dropout_prob" parameter
        SE_DROPOUT (default is 0.5) to change dropout of SentenceBertClass
        SE_LEARNING_RATE (default is 5e-5) to change the learning rate for training
        SE_WEIGHT_DECAY (default is 5e-05) to change weight decay for optimizer
        SE_EPOCH_MAX (default is 10) to change number of training epochs

    c: TargetParagraph QA: modify the parameters defined in def set_qa_statement_configuration() on line# 46
        TOP_N_ROUGE_SCORES (default is 0) (All paragaphs are selected). Enter a positive number (15  is average targetParagraph length) for selecting TOP N ROUGE score targetParagraphs
        QA_DROPOUT_HIDDEN (default is 0.3) to change BERT models "hidden_dropout_prob" parameter
        QA_DROPOUT_ATTENTION (default is 0.3) to change BERT models "attention_probs_dropout_prob" parameter
        QA_LEARNING_RATE (default is 3e-5) to change the learning rate for training
        QA_WEIGHT_DECAY (default is 0.01) to change weight decay for optimizer
        QA_EPOCH_MAX (default is 12) to change number of training epochs
        QA_MODELS (default 'roberta-base') to change underlying BERT model


## Authors

Devavrat Joshi
