# Wildfire Susceptibility Mapping

Wildfires can have significant impacts on local communities and the environment, including loss of life, damage to infrastructure, natural resources, and air pollution. Effective wildfire susceptibility mapping can help to mitigate these impacts by providing information about the likelihood of wildfire occurrence in different regions, which can inform prevention and management efforts.\
The objective of the study is to improve the current susceptibility maps that are at the municipality level, estimate correctly wildfire probabilities using supervised models and provide explainability to support decision making.

This repository contains all notebooks and instructions in order to reproduce the Machine Learning ML4Science Project 2 : 'Wildfire Susceptibility Mapping'.

`data_collection` contains the code for scrapping parts of the data and merging raster files using GDAL and rasterio.
The rest of the preprocessing was performed with a software called `QGIS` cited in our report.

`data_preprocessing` contains jupyter notebooks used to perform Exploratory Data Analysis on the dataset and display the preprocessing and feature engineering results.

In order to reproduce all the results using our preprocessed data:

- Install the environment using `pip install -r requirements.txt`

- Open the `data_preprocessing/preprocessing_cross_validation.ipynb` and run the notebook until you export the dataframe in pickle format. Pay attention to create the paths if needed.

- Open the `random_forest.ipynb` or `lightGBM.ipynb` notebook containing the complete pipeline. There are instructions on how to select the features to use for the ablation study. 

- Uncomment the grid search algorithm if needed, or directly specify the hyperparameters listed in the report.

- Wait for minutes or hours depending on the model.

- The results will be written to a .txt file. Pay attention to create the paths if needed.

- Continue running the notebook pipeline to visualize the susceptibility map and the explainability plots.

Contact us on our EPFL emails for any questions.

[Final report](ML_Project2.pdf)
