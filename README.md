# Python for Data Analysis - ESiLV A5 - 2019

This project was made using Jupyter Notebook. Librairies used are **Scikit Learn, Matplotlib, and Pandas.**

### Dataset used: _[Optical Recognition of Handwritten Digits](http://archive.ics.uci.edu/ml/datasets/Optical+Recognition+of+Handwritten+Digits)_

The goal of this dataset is to recognize a number given a handwritten number image. Images are 8x8 pixels.

Our goal is to determine which algorithm is the best performance wise, and which parameters are optimal for it.

## Results

After experimenting, it is found that the **C-Support Vector Classification** algorithm is the best algorithm performance-wise.

The algorithm classifies almost perfectly most of the numbers, but has a weakness dealing with 8s

Using Grid Search, best parameters for the algorithm are the following:

Possible parameters:

```json
{
  "kernel": ["linear", "rbf"],
  "C": [1, 2, 3, 4, 5],
  "gamma": [1, 0.1, 0.01, 0.001, 0.0001],
  "probability": [True]
}
```

Result:

```json
{
  "C": 3,
  "gamma": 0.001,
  "kernel": "rbf",
  "probability": True
}
```

### ROC Curves

![ROC Curves](https://i.imgur.com/jpTfwlT.png)
