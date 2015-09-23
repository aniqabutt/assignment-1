Assignment 1
============

This folder contains the starter files for Assignment 1, which is about solving a classification problem.

Submission is done by **pushing the necessary files to github, before the stated deadlines**. For evaluating the results (too see if you passed the required threshold) you need to **submit the output file(s) on kaggle.com too**. See the details below.

## Data

The assignment uses the Adult dataset. The task is to predict, based on census data, whether the income of an individual exceeds $50K/yr.

  - Training set: `data/adult.data`. The file contains 32561 records in total. Each line corresponds to a record, with the attributes comma separated. The last attribute is the target class label: <=50K or >50K.
  - Test set: `data/adult.test`. The file contains 16281 records. It has the exact same format as `adult.train`, except the last column. I.e., the class labels are missing from the test file; your task is to predict these and output the predictions to a separate file.
  - There are 14 attributes, a mixture of categorical and continuous ones. Mind that there are missing attribute values (denoted by ?). See the `adult.names` file under the `data` folder for further details.
  - The `eval.py` script can be used for evaluation during development (if the holdout method or cross-validation is employed).
    * The `toy_data` folder contains a toy-sized ground truth set and predictions; this is only provided to allow you to try out the evaluation script. Run `python eval.py toy_data/test.gt toy_data/test.pred` from the assignment's root folder.


### File format

The output needs to be in a CSV format, including a header line:
```
Id,Target
1,<=50K
2,<=50K
3,<=50K
4,<=50K
5,<=50K
6,>50K
7,<=50K
8,>50K
etc.
```  
where Id is the line number and Target is the prediction (<=50K or >50K).
Mind that the evaluation is case sensitive!


## Task 1

Predict the target class labels for the test data using a decision tree classifier that you implement from scratch. 

  - For each record in the test data, you need to output one line with the target label (either <=50K or >50K).
  - The output must be placed in the `output/task1.out` file. 
  - Implementing from scratch means that you are not allowed to use an existing library or package that implements decision trees.
  - You are free to pick the programming language/environment, but you are required to submit the complete source code. The code used needs to be placed in the `code` folder.  
  - The output file must be generated automatically using the decision tree approach implemented by you. Submitting predictions from any other source (Internet, another team, etc.) is considered cheating and will result in immediate disqualification (i.e., dismissal from the course).
  - To have the assignment approved, you will need to reach an **Accuracy of at least 0.8** on the test set. 
  - **Deadline: Sep 28, 23:59**


## Task 2 

Perform some data mining on the Adult dataset using the decision tree you built and write a short report describing the process and your findings.

  - The report is min 3, max 8 pages (A4) long, written in English.
    * The specific format is up to you, max font size is 12pt.
  - It needs to contain the followings:
    * Instructions on how to run your code
    * Report on any data exploration you performed (e.g., summary statistics and/or visualizations of attributes)
    * Data processing steps applied (e.g., variable transformations, feature creation)
    * How you dealt with missing attribute values
    * Looking at the first 3 levels of the decision tree, what observations can you make? Which attributes are the most important?
  - The document must be in pdf format and placed under the `report` folder.
  - **Deadline: Oct 5, 23:59**


## Task 3

This is the same as Task 1, but any existing machine learning tool/library/package may be used.

  - This task is optional. (You don't need to solve it to have the assignment approved, but you can get bonus points at the exam if you do best.)
  - The same rules apply as for Task 1, regarding supplying all source code and cheating.
  - You can submit the approach and output that you developed for Task 1.
  - The output must be placed in the `output/task3.out` file. 
  - **Deadline: Sep 28, 23:59**


## Submission

You need to submit the code, output files, and report on GitHub to the repository created for your team `uis-dat630-fall2015/{teamname}-assignment-1`.
The group name is what you provided in [this spreadsheet](https://docs.google.com/spreadsheets/d/1N5bNv3j01wFK7tiiSGH3rDyYVKjZObkmCSluMsPdHL0/edit#gid=0).

### Online evaluation and Leaderboard

To evaluate your results online you need to submit the output files on kaggle.com:

  - [Task 1 on kaggle.com](https://inclass.kaggle.com/c/uis-dat630-fall-2015-assignment-1-task-1/)
  - [Task 3 on kaggle.com](https://inclass.kaggle.com/c/uis-dat630-fall-2015-assignment-1-task-3/)
  
You need to **register using a uis.no email address** to be able to submit.
Use the same team name that you provided in the spreadsheet (i.e., the team name you also have on GitHub).

Results are considered in two categories:

  - Decision tree track -- this is for everyone, based on submissions to Task 1
  - Open track -- this is optional, based on submissions to Task 3

The best performing team for each track gets 5 bonus points at the exam (all members).


## FAQ

  - **Is it possible to submit results multiple times on kaggle?**
  Yes. Only the best performing one will be considered.
  - **Is it obligatory to submit results on kaggle?**
  No. This is just for your information to see how you perform (if you passed the Accuracy threshold) and that you can compare your performance to that of others. The final results will be based on the files pushed to GitHub (the scoring will be exactly the same).
  - **Will AutoGrader not be used then?**
  No, it will not be used for this assignment.
  - **Does everything have to be written from the ground up?**
  For the decision tree in Task 1, yes. You are allowed to use libraries for data structures and data preprocessing though.
  - **What can be used for Task 1?**
  Everything, except machine learning libraries and ready-made decision tree implementations. It is OK to look at online tutorials and examples, and to re-use them, but you will need to be able to explain every line of code you submit.
  - **What should I do if I'm feeling lost?**
  Try to build a decision tree on paper by performing the steps of the algorithm manually. (E.g., see the exercise and the solution from Lecture 5 on itslearning.) If you still feel lost, ask for help (in time, not the day before the deadline).
  - **Is it possible to get a deadline extension?**
  No. Don't even ask.
  - **Can I take the exam if I fail to complete this assignment?**
  No. So you better take it seriously.
