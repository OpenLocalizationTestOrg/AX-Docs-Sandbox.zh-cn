---
title: Demand forecasting setup | Microsoft Docs
description: This topic describes the setup tasks that you must perform to prepare for demand forecasting.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-03-30 12:35:29
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: 2094
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 72653
ms.assetid: 77ab0b46-c9e8-438d-9f3e-2d03f2188eb2
ms.region: global
ms.industry: Manufacturing
ms.author: roxanad
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 821e9a55c76316105b3eb59fb6600d5a2b2e0a33


---

# <a name="demand-forecasting-setup"></a>Demand forecasting setup

This topic describes the setup tasks that you must perform to prepare for demand forecasting.  

The setup tasks include setting up the following data and parameters.

## <a name="item-allocation-key"></a>Item allocation key
A demand forecast is calculated for an item and its dimensions only if the item is part of an item allocation key. This rule is enforced to group large numbers of items, so that demand forecasts can be created more quickly. The item allocation key percentage is ignored when demand forecasts are generated. Forecasts are created based on historical data only. An item and its dimensions must be part of only one item allocation key if the item allocation key is used during forecast creation. To add a stock keeping unit (SKU) to an item allocation key, go to **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Item allocation keys**. Use the **Assign items** page to assign an item to an allocation key.

## <a name="intercompany-planning-groups"></a>Intercompany planning groups
Demand forecasting generates cross-company forecasts. In Microsoft Dynamics 365 for Operations, companies that are planned together are grouped into one intercompany planning group. To specify, per company, which item allocation keys should be considered for demand forecasting, associate an item allocation key with the intercompany planning group member by going to **Master planning** &gt; **Setup** &gt; **Intercompany planning groups**. By default, if no item allocation keys are assigned to intercompany planning group members, a demand forecast is calculated for all items that are assigned to all item allocation keys from all Dynamics 365 for Operations companies. Additional filtering options for companies and item allocation keys are available on the **Generate statistical baseline forecast** page. Review the number of items that are forecasted. Unnecessary items might cause increased costs when you use Microsoft Azure Machine Learning.

## <a name="demand-forecasting-parameters"></a>Demand forecasting parameters
To set up demand forecasting parameters, go to **Master planning** &gt; **Setup** &gt; **Demand forecasting parameters**. Because demand forecasting runs cross-company, the setup is global. In other words, the setup applies to all companies. Demand forecasting generates the forecast in quantities. Therefore, the unit of measure that the quantity should be expressed in must be specified in the **Demand forecast unit** field. The unit of measure must be unique, to help guarantee that the aggregation and percentage distribution make sense. For more information about aggregation and percentage distribution, see [Make manual adjustments to the baseline forecast](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/master-planning/making-manual-adjustments-to-the-baseline-forecast). For every unit of measure that is used for SKUs that are included in demand forecasting, make sure that there is a conversion rule for the unit of measure and the general forecasting unit of measure. When forecast generation is run, the list of items that don't have a unit of measure conversion is logged, so that you can easily correct the setup. Demand forecasting can be used to forecast both dependent and independent demand. For example, if only the **Sales order** check box is selected, and if all the items that are considered for demand forecasting are items that are sold, the system calculates independent demand. However, critical subcomponents can be added to item allocation keys and included in demand forecasting. In this case, if the **Production line** check box is selected, a dependent forecast is calculated. There are two methods for creating a baseline forecast in Dynamics 365 for Operations. You can use forecasting models on top of historical data, or you can just copy over the historical data to the forecast. The **Forecast generation strategy** field lets you select between these two methods. To use forecast models, select **Azure Machine Learning**. By clicking **Forecast dimensions** in the left pane of the **Demand forecasting parameters** page, you can also select the set of forecast dimensions to use when the demand forecast is generated. A forecast dimension indicates the level of detail that the forecast is defined for. Company, site, and item allocation key are mandatory forecast dimensions, but you can also generate forecasts at the warehouse, inventory status, customer group, customer account, country/region, state, and item plus all item dimension levels. At any point, you can add forecast dimensions to the list of dimensions that are used for demand forecasting. You can also remove forecast dimensions from the list. However, manual adjustments are lost if you add or remove a forecast dimension. Not all items behave in the same manner from a demand forecasting perspective. Similar items can be grouped in one item allocation key, and parameters such as transaction types and forecast method settings can be set per item allocation key. Click **Item allocation keys** in the left pane of the **Demand forecasting parameters** page. To generate the forecast, Dynamics 365 for Operations uses a Machine Learning web service. To connect to the service, you must provide Dynamics 365 for Operations the following information if you sign in to Microsoft Azure Machine Learning Studio:

-   Web service application programming interface (API) key
-   Web service endpoint URL
-   Azure storage account name
-   Azure storage account key

**Note:** The Azure storage account name and key are required only if you use a custom storage account. If you deploy the on-premises version, you must have a custom storage account on Azure, so that the Machine Learning service can access the historical data. To create demand predictions, you can deploy your own service by using Machine Learning Studio or the Dynamics 365 for Operations demand forecasting experiments. Instructions for deploying the Dynamics 365 for Operations demand forecasting experiments as a web service are available Dynamics 365 for Operations. On the **Demand forecasting parameters** page, click the **Azure Machine Learning** tab.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Settings for the Dynamics 365 for Operations demand forecasting machine learning service
To view the parameters that can be configured for the Dynamics 365 for Operations demand forecasting service, go to **Master Planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Forecasting algorithm parameters**. The **Forecasting algorithm parameters** page shows the default values for the parameters. You can overwrite these parameters on the **Demand forecasting parameters** page. Use the **General** tab to overwrite the parameters globally, or use the **Item allocation keys** tab to overwrite the parameters per item allocation key. Parameters that are overwritten for an item allocation key affect only the forecast of items that are associated with that item allocation key.

<a name="see-also"></a>See also
--------

[Introduction to demand forecasting](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/master-planning/introduction-to-dynamics-ax7-demand-forecasting)

[Generating a statistical baseline forecast](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/master-planning/generating-a-statistical-baseline-forecast)

[Making manual adjustments to the baseline forecast](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/master-planning/making-manual-adjustments-to-the-baseline-forecast)




<!--HONumber=Feb17_HO3-->


