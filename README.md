# A framework of PERformance METRICS (PerMetrics) for artificial intelligence models
[![GitHub release](https://img.shields.io/badge/release-1.0.1-yellow.svg)]()
[![Wheel](https://img.shields.io/pypi/wheel/gensim.svg)](https://pypi.python.org/pypi/permetrics) 
[![PyPI version](https://badge.fury.io/py/permetrics.svg)](https://badge.fury.io/py/permetrics)
[![DOI](https://zenodo.org/badge/280617738.svg)](https://zenodo.org/badge/latestdoi/280617738)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

---
> "Knowledge is power, sharing it is the premise of progress in life. It seems like a burden to someone, but it is the only way to achieve immortality."
>  --- [Thieu Nguyen](https://www.researchgate.net/profile/Thieu_Nguyen6)
---

## Introduction
* PerMetrics is a python library for performance metrics of artificial intelligence models.

* The goals of this framework are:
    * Combine all metrics for regression, classification and clustering models
    * Helping users in all field access to metrics as fast as possible
    * Perform Qualitative Analysis of models.
    * Perform Quantitative Analysis of models.

* Metrics

| Problem        | STT | Metric Short Name | Metric Fullname                           |
|----------------|-----|-------------------|-------------------------------------------|
| Regression     | 1   | EVS               | Explained Variance Score                  |
|                | 2   | ME                | Max Error                                 |
|                | 3   | MAE               | Mean Absolute Error                       |
|                | 4   | MSE               | Mean Squared Error                        |
|                | 5   | RMSE              | Root Mean Squared Error                   |
|                | 6   | MSLE              | Mean Squared Log Error                    |
|                | 7   | MedAE             | Median Absolute Error                     |
|                | 8   | MRE               | Mean Relative Error                       |
|                | 9   | MAPE              | Mean Absolute Percentage Error            |
|                | 10  | SMAPE             | Symmetric Mean Absolute Percentage Error  |
|                | 11  | MAAPE             | Mean Arctangent Absolute Percentage Error |
|                | 12  | MASE              | Mean Absolute Scaled Error                |
|                | 13  | NSE               | Nash\-Sutcliffe Efficiency Coefficient    |
|                | 14  | WI                | Willmott Index                            |
|                | 15  | R                 | Pearson’s Correlation Index               |
|                | 16  | CI                | Confidence Index                          |
|                | 17  | R2                | Coefficient of Determination              |
| Classification | 1   |                   |                                           |
| Clustering     | 1   |                   |                                           |



### Dependencies
* Python (>= 3.7)
* Numpy (>= 1.15.1)


### User installation
Install the [current PyPI release](https://pypi.python.org/pypi/permetrics):

```bash
pip install permetrics
```

Or install the development version from GitHub:

```bash
pip install git+https://github.com/thieunguyen5991/permetrics
```


### Example
+ All you need to do is: (Make sure your y_true and y_pred is a numpy array)

```code 
* Simple example:

## For example with RMSE:

    from numpy import array
    from permetrics.regression import Metrics
    
    ## For 1-D array
    y_true = array([3, -0.5, 2, 7])
    y_pred = array([2.5, 0.0, 2, 8])
    
    obj1 = Metrics(y_true, y_pred)
    print(obj1.rmse_func(clean=True, decimal=5))
    
    ## For > 1-D array
    y_true = array([[0.5, 1], [-1, 1], [7, -6]])
    y_pred = array([[0, 2], [-1, 2], [8, -5]])
    
    multi_outputs = [None, "raw_values", [0.3, 1.2], array([0.5, 0.2]), (0.1, 0.9)]
    obj2 = Metrics(y_true, y_pred)
    for multi_output in multi_outputs:
        print(obj2.rmse_func(clean=False, multi_output=multi_output, decimal=5))

* Or run the simple:
    python examples/RMSE.py

* The more complicated tests in the folder: examples
```
The [documentation](https://permetrics.readthedocs.io/) includes more detailed installation instructions and explanations.

### Changelog
* See the [ChangeLog.md](https://github.com/thieunguyen5991/permetrics/blob/master/ChangeLog.md) for a history of notable changes to permetrics.


### Important links

* Official source code repo: https://github.com/thieunguyen5991/permetrics
* Official documentation: https://permetrics.readthedocs.io/
* Download releases: https://pypi.org/project/permetrics/
* Issue tracker: https://github.com/thieunguyen5991/permetrics/issues

* This project also related to my another projects which are "meta-heuristics" and "neural-network", check it here
    * https://github.com/thieunguyen5991/opfunu
    * https://github.com/thieunguyen5991/metaheuristics
    * https://github.com/chasebk
    
   
## Contributions 

### Citation
+ If you use permetrics in your project, please cite my works: 
```code 
@software{thieu_nguyen_2020_3951205,
  author       = {Thieu Nguyen},
  title        = {A framework of PERformance METRICS (PerMetrics) for artificial intelligence models},
  month        = jul,
  year         = 2020,
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.3951205},
  url          = {https://doi.org/10.5281/zenodo.3951205}
}

@article{nguyen2019efficient,
  title={Efficient Time-Series Forecasting Using Neural Network and Opposition-Based Coral Reefs Optimization},
  author={Nguyen, Thieu and Nguyen, Tu and Nguyen, Binh Minh and Nguyen, Giang},
  journal={International Journal of Computational Intelligence Systems},
  volume={12},
  number={2},
  pages={1144--1161},
  year={2019},
  publisher={Atlantis Press}
}
```
 
