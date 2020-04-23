### Lab 12 Model evaluation and Improvement

For this week lab, study the exampeles in the notebook "[05-model-evaluation-and-improvement.ipynb](05-model-evaluation-and-improvement.ipynb)" since we dont cover it in the class. It is a compressed version from the textbook materials.

Additionally, a small model selection experiment is included in this lab. 

#### Using Grid Search for parameter tuning
Use the [GridSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html) to find optimal parameters for machine learning model for the [breast cancer dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html#sklearn.datasets.load_breast_cancer). For this exercise try to find the optimal parametesrs for SVC with linear and rbf kernels. The documentation for the SVC kernels is available [here](https://scikit-learn.org/stable/modules/svm.html#kernel-functions)