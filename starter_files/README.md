
# Operationalizing Machine Learning

## Overview of project
This is the second of three projects required for the fulfilment of the Microsoft Azure Machine Learning Nanodegree program with Udacity.

This project entails configuring a cloud-base machine learning production model, deploy it, and consume it. It also covers the creation, publishing, and consumption of a machine learning pipeline.

## Summary of dataset
This dataset contains data from a direct marketing campaign through phone calls of a Portuguese banking institution. The classification goal is to predict if a client will subscribe to one of the bank's product, bank term deposit, represented by the variable, y. 
	
At pristine state, the dataset contains 20 different predictor variable and 32950 rows representing different customers with 3,692 subscribing to the bank's product and 29,258 negative classes.

Click [here](https://archive.ics.uci.edu/ml/datasets/bank+marketing) for detailed information about the dataset.

Click [here](https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv) to download the dataset.


## Architectural Diagram

![Project Architecture](Images/architecture.png)

The project architecture as shown above consist of six major steps.
#### Authentication
This involves creating a ``service principal`` user role account with controlled permissions to access specific resorces; hence, providing security. The Azure ML Extension would have to be installed for this to be possible. In this project, this was skipped because the Udacity workspace was used; however, if i were to use a private Azure account, it would be necessary.

#### AutoML model
After enabling security and completing authentication, an AutoML model would be trained. Register the dataset,create an experiment, and configure a compute cluster to run the experiment.

#### Deploy the best model
Deployment is about delivering a trained model into production so that it can be consumed by others. The best model from the completed automl experiment run is deployed to interact with the HTTP API service. It was deployed into an Azure Container Instance (ACI) which offers a container technology to quickly deploy compute instances. Authentication is also enabled at this point. 

#### Enable logging
Logging is a core pillar of MLOps. It gives information on how deployed services (in this case model) are behaving over time. Enabling application insight helps to fulfil this purpose. Detection of anomalies, performance visualization, and log retrieval can be done using the Python SDK.

#### Consume model endpoints
Deployed models in Azure exposes HTTP endpoint that allows interacting with it. Swagger documentation and benchmarking was done. Swagger is a tool that helps build, document, and consume RESTful web services. It ensures easier and more confident interaction and explains what type of requests an API can consume: ``POST`` and ``GET``. Meanwhile, benchmark is an acceptable performance measure essential for enhancing performance and detecting anomalies.

#### Create and publish a pipeline
Pipelines are a great way to automate workflows. Published pipelines allow external services to interact with them so that they can do work more efficiently.

## Key Steps
*TODO*: Write a short discription of the key steps. Remeber to include all the screencasts required to demonstrate key steps. 

*TODO* Remeber to provide screenshots of the `RunDetails` widget as well as a screenshot of the best model trained with it's parameters.

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
