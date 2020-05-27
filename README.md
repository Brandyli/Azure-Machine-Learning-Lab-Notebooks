# Azure-Machine-Learning-Lab-Notebooks

## Getting Started with Azure Machine Learning
In this exercise, you will create the Azure Machine Learning workspace and a compute instance, and clone the lab files to your workspace. You'll then run a simple Python experiment in your workspace.

## Before You Start
Azure Machine Learning (Azure ML) is a Microsoft Azure-based service for running data science and machine learning workloads at scale in the cloud. To use Azure Machine Learning, you will need an Azure subscription. If you do not already have one, you can sign up for a free trial at https://azure.microsoft.com.

## Create an Azure Machine Learning Workspace
Sign into the Azure portal and create a new resource - search for "machine learning" and select Machine Learning. Specify a unique workspace name, create a new resource group in the region nearest to your location, and select the Enterprise workspace edition.
<img width="1435" alt="Screen Shot 2020-05-27 at 6 48 10 PM" src="https://user-images.githubusercontent.com/46945617/83079832-b4d36b80-a04a-11ea-9838-c458a5749679.png">

## Create a Compute Instance
You can perform many machine learning tasks in the Studio interface, but it's also important to be able to script configuration tasks and data experiments to make them easier to repeat and automate. Compute Instances provide a virtual machine that you can use as a hosted development workstation to do this.

In the Azure Machine Learning studio web interface for your workspace, view the Compute page. This is where you'll manage all the compute targets for your data science activities.

On the Compute Instances tab, add a new compute instance, giving it a unique name and using the CPU virtual machine type and STANDARD_DS3_V2 virtual machine size. You'll use this VM as a development environment.

If necessary, click Refresh periodically until the compute instance you created has started. Then click its Jupyter link to open Jupyter Notebooks on the VM.

In the notebook environment, on the New menu, click Terminal. This will open a new tab with a command shell.

The Azure Machine Learning SDK is already installed in the compute instance image, but it's worth ensuring you have the latest version, with the optional packages you'll need in this lab; so enter the following command to update the SDK packages:
Next, run the following commands to change the current directory to the Users directory, and retrieve the notebooks you will use in this lab:
```
pip install --upgrade azureml-sdk[notebooks,automl,explain]

```

