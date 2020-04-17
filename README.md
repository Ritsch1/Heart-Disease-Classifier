# Heart-Disease-Classifier
Building a machine learning binary-classification model to predict whether or not a patient has heart-disease.

## Content

* [Tools used](#tools)
* [Data used](#data)
* [Preview graphical insights](#preview-graphical-insights-from-the-dataset)
* [Work with the project](#work-with-the-project)
* [Use the model](#use-the-model)

## Tools
The tools used in this project are:

* numpy
* pandas
* matplotlib
* scikit-learn
* Jupyter

## Data

TThe data I will be using is from [kaggle](https://www.kaggle.com/ronitf/heart-disease-uci).
The original dataset from the [Cleveland database](https://archive.ics.uci.edu/ml/datasets/heart+Disease) contained way more than 14 features.

For more details please look into the [jupyter notebook](https://github.com/Ritsch1/Heart-Disease-Classifier/blob/development/notebooks/Heart-Disease-Classification.ipynb) or into the [data](https://github.com/Ritsch1/Heart-Disease-Classifier/tree/development/data) folder.

## Preview: Graphical insights from the dataset 

At this point I share some of the insights the EDA revealed. For further graphical insights please 
look into the [jupyter notebook](https://github.com/Ritsch1/Heart-Disease-Classifier/blob/development/notebooks/Heart-Disease-Classification.ipynb) or into the [plots](https://github.com/Ritsch1/Heart-Disease-Classifier/tree/development/plots) folder.

**Previews**

* This scatter plot shows the relation between the age and the maximal heart rate of a patient.

<img src="plots/ratio_age_maxHeartRate.png" height="300" width="650">

* This correlation - matrix shows the correlation of the medical features of a patient and his diagnosis.

<img src="plots/correlation_matrix_features.png" height="400" width="550">

## Work with the project

The [environment.yml](https://github.com/Ritsch1/Heart-Disease-Classifier/blob/development/environment.yml) contains the 
conda environment(the tools) being used in this project. 
There are several ways to build the environment in order to work with the notebook in this project.

1. From scratch:
* `conda create --prefix ./env pandas numpy matplotlib scikit-learn jupyter`

1. From environment.yml file:
* `conda env create --prefix -f ./env -f Path/to/yaml/file`

Each of those commands will create the environment within an env-folder relative to your current directory.

2. When you have successfully created your environment folder you can list all your environments with:

`conda env list`

3. You then have to activate the environment using:

`conda activate path/to/your/environment/folder`

If successfull, the base - prompt should change to your environment-path.

4. Then you can run `jupyter notebook` from within the anaconda prompt which should open a jupyter dashboard in your default-browser.

From that you can open the jupyter notebook and work with it.

## Use the model

The model trained in this project is saved in the [model folder](https://github.com/Ritsch1/Heart-Disease-Classifier/blob/development/model) as a binary object.

It was saved as a binary with the [pickle library](https://docs.python.org/3/library/pickle.html).
If you want to use the model for predictions on it's own, it would be best to use the `pickle` method `load` for it.
