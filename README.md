### Important things to take into account

- Do not take more than 4 hours to do this exercise. We will only take into
account the work you have done until the 4th hour.
- You can use python3 and pip3 to install stuff. You can make use of virtualenv and virtualenvwrapper.
- If you run into system problems, you can stop and let us now so that we can
fix it before you continue.
- Use git to track your changes, so that we can follow the steps you did during the implementation.

### Background

dataset.zip contains the dataset you will use. It is a twitter dataset
labeled for sentiment analysis. It contains two files:

- test.csv: your test data
- training.csv: your training data

Each file contains the following columns:

1. target: the polarity of the tweet (0 = negative, 2 = neutral, 4 = positive)
2. ids: The id of the tweet ( 2087)
3. date: the date of the tweet (Sat May 16 23:58:44 UTC 2009)
4. flag: The query (lyx). If there is no query, then this value is NO_QUERY.
5. user: the user that tweeted (robotickilldozr)
6. text: the text of the tweet (Lyx is cool)

### Goal

Your goal is to build a model which is able to predict the sentiment of tweets.

### Instructions

1. Create a bash script "preprocess.sh" which is able to:
  1.1 Decompress dataset.zip
  1.2 Preprocess training.csv: we only want to keep the first column (label)
      and the sixth (the tweet).
  1.3 Do the same with test.csv. Also, filter it so that we only have samples
      with labels 0 (negative) and 4 (positives). We are removing the neutral
      labels for simplicity.

(NOTE: we value some fluidity in basic command-line utilities, that's why we
ask you to do this preprocessing within a bash script. If you feel unable to do
it, you can resort to python for this).

2. Create a script "train_model.py" which can be executed to:
- Load the data
- Train a model on the train data.
- Evaluate the model on the test data.
- Save the model to a file.
- Report the metrics by standard output.

This script can import stuff from other python files, if you want to.

3. We'd like to be able to run all the process (preprocessing + training) by
just typing "make".

4. Write a TODO.md file explaining what next steps you would take to finish
or improve the system.

### What will we evaluate?

- We do not care about the accuracy of the model.
- We care about clean, commented and organized code.
- We also care about models and metrics which make sense for this task.
- Use whatever library you want, and google whatever you need.