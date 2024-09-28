# datasciencee2e
## Workshop for learning Fabric Data Science

Welcome to the Microsoft Fabric Data Science end-to-end workshop. The purpose of the workshop is to bring you up to speed on some of the Data Science tools and other experiences in Microsoft Fabric including Lakehouse, Spark Notebooks, MLFlow, and Semantic Models and Power BI reports.

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

### Prereqs

Prior to starting the hands-on activites you please clone this GitHub repo to your local machine by cutting and pasting and running this command.

```    
git clone https://github.com/DataSnowman/datasciencee2e.git
```

`Note` you can also download these repo files by clicking on the green `Code` button and selecting `Download ZIP`

![gitclone](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/gitclone.png)

### Workshop

The Workshop is broken up into five parts:

* [Tutorial Part 1: Ingest data into a Microsoft Fabric lakehouse using Apache Spark](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-ingest-data)
* [Tutorial Part 2: Explore and visualize data using Microsoft Fabric notebooks](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-explore-notebook)
* [Tutorial Part 3: Train and register a machine learning mode](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-train-models)
* [Tutorial Part 4: Perform batch scoring and save predictions to a lakehouse](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-batch-scoring)
* [Tutorial Part 5: Visualize predictions with a Power BI report](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-create-report)

## Login

In your browser (Incognito, InPrivate, Private if you are not using your company Fabric Tenant) cut and paste this Link

```
https://fabric.microsoft.com/
```
 
Enter the userid (Email) assigned for you to use during the workshop and click `Submit`

![login1](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/login1.png)

Enter the password provided by the instructor and click `Sign in`

![login2](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/login2.png)

This should land you on a home page that looks like this:

![landing](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/landing.png)

## Create a new Lakehouse in your Fabric workspace

To get started click on the Microsoft Fabric icon in the bottow left corner of the browser.  Click on `Data Science`

![datascience](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/datascience.png)

Now click on Workspaces to find your Fabric workspace.  You should have a workspace precreated for you.

![workspace](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/workspace.png)

When you open the workspace it should be empty and look something like this:

![user1ws](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/user1ws.png)

Create a new Lakehouse by clicking `+New` and selecting `Lakehouse`

![lh1](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/lh1.png)

Name the Lakehouse something like `ChurnanAlysis` since this lakehouse will used to collect .  Click `Create`

![newlh](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/newlh.png)

The empty lakehouse should look like this with empty Tables and Files folders

![lhtablesfiles](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/lhtablesfiles.png)

## Import tutorial notebooks

We utilize the notebook item in the Data Science experience to demonstrate various Fabric capabilities. The notebooks are available as Jupyter notebook files that can be imported to your Fabric-enabled workspace.

1. Download your notebook(s).  If you have not already done so in the Prereqs section make sure to download the files by cloning the GitHub Repo 

```    
git clone https://github.com/DataSnowman/datasciencee2e.git
```

`Note` you can also download these repo files by clicking on the green `Code` button and selecting `Download ZIP`
 
2. On the Data science experience homepage, select **Import notebook** and upload the notebook files that you downloaded in Prereqs or step 1.

![importnotebooks](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/importnotebooks.png)

![uploadnotebooks](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/uploadnotebooks.png)

3. Once the notebooks are imported, select **Go to workspace** in the import dialog box.

4. The imported notebooks are now available in your workspace for use.

![allnotebooks](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/allnotebooks.png)

5. If the imported notebook includes output, select the **Edit** menu, then select **Clear all output(s)**.

![clearalloutputs](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/clearalloutputs.png)

## Attach a lakehouse to the notebooks

To demonstrate Fabric lakehouse features, many of the tutorials require attaching a default lakehouse to the notebooks. The following steps show how to add a lakehouse to a notebook in a Fabric-enabled workspace.

> [!NOTE]
> Before executing each notebooks, you need to perform these steps on that notebook. 

1. Open the notebook in the workspace.

2. Select **Add lakehouse** in the left pane.

![addlh](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/addlh.png)

3. Create a new lakehouse or use an existing lakehouse.
    1. To create a new lakehouse, select **New**. Give the lakehouse a name and select **Create**.
    2. To use an existing lakehouse, select **Existing lakehouse** to open the **Data hub** dialog box. Select the lakehouse you want to use and then select **Add**.

4. Once a lakehouse is added, it's visible in the lakehouse pane and you can view tables and files stored in the lakehouse.

![lhadded](https://raw.githubusercontent.com/datasnowman/datasciencee2e/main/images/lhadded.png)

## Work through parts 1 - 5

## [Tutorial Part 1: Ingest data into a Microsoft Fabric lakehouse using Apache Spark](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-ingest-data)

## [Tutorial Part 2: Explore and visualize data using Microsoft Fabric notebooks](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-explore-notebook)

## [Tutorial Part 3: Train and register a machine learning mode](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-train-models)

## [Tutorial Part 4: Perform batch scoring and save predictions to a lakehouse](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-batch-scoring)

## [Tutorial Part 5: Visualize predictions with a Power BI report](https://learn.microsoft.com/en-us/fabric/data-science/tutorial-data-science-create-report)

## `Congrats you have completed the Microsoft Fabric Data Science end-to-end workshop`