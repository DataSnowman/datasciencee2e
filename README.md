# datasciencee2e
Easy to get Jupyter Notebooks for Fabric Data Science

## Workshop for learning Fabric Data Science

Welcome to the Microsoft Fabric Data Science end-to-end workshop.  The purpose of the workshop is to bring you up to speed on some of the Data Science tools and other experiences in Microsoft Fabric including Lakehouse, Spark Notebooks, MLFlow, and Semantic Models and Power BI reports.

### Datasets

The dataset contains churn status of 10,000 customers. It also includes attributes that could impact churn such as:

* Credit score
* Geographical location (Germany, France, Spain)
* Gender (male, female)
* Age
* Tenure (years of being bank's customer)
* Account balance
* Estimated salary
* Number of products that a customer has purchased through the bank
* Credit card status (whether a customer has a credit card or not)
* Active member status (whether an active bank's customer or not)

The dataset also includes columns such as row number, customer ID, and customer surname that should have no impact on customer's decision to leave the bank. 

The event that defines the customer's churn is the closing of the customer's bank account. The column `exited` in the dataset refers to customer's abandonment. There isn't much context available about these attributes so you have to proceed without having background information about the dataset. The aim is to understand how these attributes contribute to the `exited` status.

Example rows from the dataset:

|"CustomerID"|"Surname"|"CreditScore"|"Geography"|"Gender"|"Age"|"Tenure"|"Balance"|"NumOfProducts"|"HasCrCard"|"IsActiveMember"|"EstimatedSalary"|"Exited"|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|15634602|Hargrave|619|France|Female|42|2|0.00|1|1|1|101348.88|1|
|15647311|Hill|608|Spain|Female|41|1|83807.86|1|0|1|112542.58|0|

The Dataset will be imported when you run the first Notebook `1-ingest-data.ipynb`

### Workshop

The Workshop is broken up into five parts:

* [Tutorial Part 1: Ingest data into a Microsoft Fabric lakehouse using Apache Spark](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-ingest-data)
* [Tutorial Part 2: Explore and visualize data using Microsoft Fabric notebooks](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-explore-notebook)
* [Tutorial Part 3: Train and register a machine learning mode](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-train-models)
* [Tutorial Part 4: Perform batch scoring and save predictions to a lakehouse](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-batch-scoring)
* [Tutorial Part 5: Visualize predictions with a Power BI report](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-create-report)

Prior to starting the hands-on activites you please clone this GitHub repo to your local machine by cutting and pasting and running this command.

```    
git clone https://github.com/DataSnowman/datasciencee2e.git
```

`Note` you can also download these repo files by clicking on the green `Code` button and selecting `Download ZIP`

![gitclone](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/gitclone.png)


## Login

In your browser (Incognito, InPrivate, Private if you are not using your company Fabric Tenant) cut and paste this Link

```
https://fabric.microsoft.com/
```
 
Enter the userid (Email) assigned for you to use during the workshop and click `Submit`

![login1](https://raw.githubusercontent.com/datasnowman/shapedata/main/images/login1.png)

Enter the password provided by the instructor and click `Sign in`

![login2](https://raw.githubusercontent.com/datasnowman/shapedata/main/images/login2.png)

This should land you on a home page that looks like this:

![landing](https://raw.githubusercontent.com/datasnowman/shapedata/main/images/landing.png)

## Create a new Lakehouse in your Fabric workspace

To get started you can click on any of the experiences on the home page or on the Microsoft Fabric icon in the bottow left corner of the browser.  For example click on `Data Factory` or `Data Engineering`

![datafactory](https://raw.githubusercontent.com/datasnowman/shapedata/main/images/datafactory.png)

Now click on Workspaces to find your Fabric workspace.  Please click on the workspace that is the same as the userid (email i.e. user1 or user2, etc) you logged on as.

![workspace](https://raw.githubusercontent.com/datasnowman/shapedata/main/images/workspace.png)

When you open the workspace it should be empty and look something like this:

![user1ws](https://raw.githubusercontent.com/datasnowman/shapedata/main/images/user1ws.png)

Create a new Lakehouse by clicking `+New` and selecting `Lakehouse`

![lh1](https://raw.githubusercontent.com/datasnowman/shapedata/main/images/lh1.png)

Name the Lakehouse something like `MRT` since this lakehouse will used to collect and analyze public Taipei Mass Rapid Transit (MRT) data.  Click `Create`

![newlh](https://raw.githubusercontent.com/datasnowman/shapedata/main/images/newlh.png)

The empty lakehouse should look like this with empty Tables and Files folders

![mrttablesfiles](https://raw.githubusercontent.com/datasnowman/shapedata/main/images/mrttablesfiles.png)


## [Tutorial Part 1: Ingest data into a Microsoft Fabric lakehouse using Apache Spark](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-ingest-data)

## [Tutorial Part 2: Explore and visualize data using Microsoft Fabric notebooks](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-explore-notebook)

## [Tutorial Part 3: Train and register a machine learning mode](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-train-models)

## [Tutorial Part 4: Perform batch scoring and save predictions to a lakehouse](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-batch-scoring)

## [Tutorial Part 5: Visualize predictions with a Power BI report](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-create-report)

## `Congrats you have completed the Microsoft Fabric Data Science end-to-end workshop`