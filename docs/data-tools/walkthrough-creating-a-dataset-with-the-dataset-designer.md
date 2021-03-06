---
title: "Walkthrough: Creating a Dataset with the Dataset Designer | Microsoft Docs"
ms.custom: ""
ms.date: "11/02/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "datasets [Visual Basic], walkthroughs"
  - "XML schemas, creating datasets"
  - "data [Visual Studio], Dataset Designer"
  - "Dataset Designer, walkthroughs"
  - "datasets [Visual Basic], creating"
ms.assetid: 12360f54-db6c-45d2-a91f-fee43214b555
caps.latest.revision: 19
author: "gewarren"
ms.author: "gewarren"
manager: "ghogen"
robots: noindex,nofollow
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Walkthrough: Creating a Dataset with the Dataset Designer
In this walkthrough you will create a dataset using the **Dataset Designer**. It will take you through the process of creating a new project and adding a new **DataSet** item to it. You will learn how to create tables based on tables in a database without using a wizard.  
  
 Tasks illustrated in this walkthrough include:  
  
-   Creating a new **Windows Forms Application** project.  
  
-   Adding an empty **DataSet** item to the project.  
  
-   Creating and configuring a data source in your application by building a dataset with the **Dataset Designer**.  
  
-   Creating a connection to the Northwind database in **Server Explorer**.  
  
-   Creating tables with TableAdapters in the dataset based on tables in the database.  
  
 [!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]  
  
## Prerequisites  
In order to complete this walkthrough, you need:  
  
-   Access to the Northwind sample database (SQL Server or Access version). For more information, see [How to: Install Sample Databases](../data-tools/installing-database-systems-tools-and-samples.md).  
  
## Creating a New Windows Forms Application Project  
  
#### To create a new Windows Forms Application project  
  
1. In Visual Studio, on the **File** menu, select **New**, **Project...**.  
  
2. Expand either **Visual C#** or **Visual Basic** in the left-hand pane, then select **Windows Classic Desktop**.  

3. In the middle pane, select the **Windows Forms App** project type.  

4. Name the project **DatasetDesignerWalkthrough**, and then choose **OK**. 
  
     The **DatasetDesignerWalkthrough** project is created, and added to **Solution Explorer**.  
  
## Adding a New Dataset to the Application  
  
#### To add a new dataset item to the project  
  
1.  On the **Project** menu, click **Add New Item**.  
  
     The **Add New Item** dialog box appears.  
  
2.  In the **Templates** box of the **Add New Item** dialog box, click **DataSet**.  
  
3.  Name the Dataset `NorthwindDataset`, and then click **Add**.  
  
     [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] will add a file called **NorthwindDataset.xsd** to the project and open it in the **Dataset Designer**.  
  
## Creating a Data Connection in Server Explorer  
  
#### To create a connection to the Northwind database  
  
1.  On the **View** menu, click **Server Explorer**.  
  
2.  In **Server Explorer**, click the **Connect to Database** button.  
  
3.  Create a connection to the Northwind sample database.  
  
    > [!NOTE]
    >  You can connect to the SQL Server or Access version of Northwind for this walkthrough.  
  
## Creating the Tables in the Dataset  
This section explains how to add tables to the dataset.  
  
#### To create the Customers table  
  
1.  Expand the data connection you created in **Server Explorer**, and then expand the **Tables** node.  
  
2.  Drag the **Customers** table from **Server Explorer** onto the **Dataset Designer**.  
  
     A **Customers** data table and **CustomersTableAdapter** are added to the dataset.  
  
#### To create the Orders table  
  
-   Drag the **Orders** table from **Server Explorer** onto the **Dataset Designer**.  
  
     An **Orders** data table, **OrdersTableAdapter**, and data relation between the **Customers** and **Orders** tables are added to the dataset.  
  
#### To create the OrderDetails table  
  
-   Drag the **Order Details** table from **Server Explorer** onto the **Dataset Designer**.  
  
     An **Order Details** data table, **OrderDetailsTableAdapter**, and a data relation between the **Orders** and **OrderDetails** tables are added to the dataset.  
  
## Next Steps  
  
### To add functionality to your application  
  
-   Save the dataset.  
  
-   Select items in the **Data Sources** window and drag them onto a form. For more information, see [Bind Windows Forms controls to data in Visual Studio](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md).  
  
-   Add more queries to the TableAdapters. 
  
-   Add validation logic to the <xref:System.Data.DataTable.ColumnChanging> or <xref:System.Data.DataTable.RowChanging> events of the data tables in the dataset. For more information, see [Validate data in datasets](../data-tools/validate-data-in-datasets.md).  
  
## See Also  
 [Bind Windows Forms controls to data in Visual Studio](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md)   
 [Bind controls to data in Visual Studio](../data-tools/bind-controls-to-data-in-visual-studio.md)   
 [Validating Data](validate-data-in-datasets.md)   
 [Saving Data](../data-tools/saving-data.md)