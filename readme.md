# Titanic predictions

This project is a solution for the [*Titanic: Machine Learning from Disaster*](https://www.kaggle.com/c/titanic), a competition from Kaggle. The goal is that given a set gathered data about passagers which we know if they survived or not, then predict which of the passagers in another set have survived.

## Project structure

```
/titanic-predictions | main folder
    /data            | data directly downloaded from Kaggle
    /notebooks       | exploratory data analysis, inferences and tests
    /scripts         | utils for managing this project
```

## Notebooks

Under the folder *notebooks*, you'll find all the work on trial/error for this project. Here is an explanation of each one:

* **exploratory-data-analysis.ipynb** explores the data using different sorts of charts and checks variation and deviation to see what variables may be useful to our models. It also gives a look to the data: what does it contain? what is the probability of a female to survive?

* **svm-model.ipynb** trains a simple SVM with rbf kernel, the missing values on age, fare and embaked columns are filled with the mean. This model produces about 0.67 score out of 1.

* **enhancing-model-pipeline.ipynb** presents a more refined pipele and trains an SVM with polynomial kernel to predict if a person will survive. The missing values are previously predicted using other SVM (classification) for the embarked port and SVR (regression for fare and age, continuous values). This model produces an output of 0.77 score out of 1.
