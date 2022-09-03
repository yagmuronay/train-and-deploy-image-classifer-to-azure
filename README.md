# Train and deploy an image classification model to Azure ML

In this project, you will train and deploy an image classification model using the [MNIST](https://docs.microsoft.com/azure/open-datasets/dataset-mnist)
dataset with following steps:

- Download a dataset and look at the data.
- Train an image classification model and log metrics using MLflow.
- Deploy the model to do real-time inference.


## Prerequisites

Before you start, you need to complete the [Quickstart: Get started with Azure Machine Learning](https://docs.microsoft.com/en-us/azure/machine-learning/quickstart-create-resources)  to:

- Create a workspace.
- Create a cloud-based compute instance to use for your development environment.

If you want to secure your Azure Machine Learning workspace and its associated resources in a virtual network, you can follow the steps in [Secure an Azure Machine Learning workspace with virtual networks](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-secure-workspace-vnet?tabs=pe%2Ccli). Then you can run the notebook from your Azure ML workspace. 

If you want to create your own environment, install the required packages as follows:

	pip install -r requirements.txt

## Training and Deployment
Copy the notebook train_adeploy_image_cllasifier.ipynb in this folder to train and deploy the model. You will also send a http request to get the real-time inference. The last cell will delete API service.

If you want to control cost further, stop the compute instance by selecting the "Stop compute" button next to the Compute dropdown. Then start the compute instance again the next time you need it. 

### View endpoint
Once the model has been successfully deployed, you can view the endpoint by navigating to Endpoints in the left-hand menu in Azure Machine Learning studio. You will be able to see the state of the endpoint (healthy/unhealthy), logs, and consume (how applications can consume the model).


## Clean up

If you don't plan to use any of the resources that you created, delete them so you don't incur any charges:

- In the Azure portal, select Resource groups on the far left.
- From the list, select the resource group that you created.
- Select Delete resource group.
- Enter the resource group name. Then select Delete.

