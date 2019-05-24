# The Simple Guide to Data Science with Python

_Data Science with Python explained simply._

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/siowyisheng/simple-data-science/blob/master/LICENSE) ![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)

## Table of Contents <!-- omit in toc -->

- [What is Data Science?](#what-is-data-science)
- [What does Data Science look like?](#what-does-data-science-look-like)

## What is Data Science?

## What does Data Science look like?

### How to split a dataset into training and test datasets?

https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html

## How to work with unstructured text data?

https://machinelearningmastery.com/prepare-text-data-machine-learning-scikit-learn/

## What is the bag of words model?

https://machinelearningmastery.com/gentle-introduction-bag-words-model/

https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.CountVectorizer.html
is a good way to implement it, and you can choose ngrams in the argument.

## Speed

https://engineering.upside.com/a-beginners-guide-to-optimizing-pandas-code-for-speed-c09ef2c6a4d6

## How to combine multiple models into one?

https://scikit-learn.org/stable/modules/ensemble.html

## Troubleshooting

### Kernel is using a different environment!

https://stackoverflow.com/questions/37891550/jupyter-notebook-running-kernel-in-different-env

## How to ensemble models?

You can ensemble models which work on different features like this.

```python
model1 = tree.DecisionTreeClassifier()
model2 = KNeighborsClassifier()
model3 = LogisticRegression()

model1.fit(x_train,y_train)
model2.fit(x_train,y_train)
model3.fit(x_train,y_train)

pred1 = model1.predict_proba(x_test)
pred2 = model2.predict_proba(x_test)
pred3 = model3.predict_proba(x_test)

finalpred = (pred1*0.3+pred2*0.3+pred3*0.4)
```

[Source](https://www.analyticsvidhya.com/blog/2018/06/comprehensive-guide-for-ensemble-models/)
