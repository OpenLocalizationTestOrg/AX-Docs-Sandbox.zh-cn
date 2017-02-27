---
title: Generate a statistical baseline forecast
description: This article provides information about the parameters and filters that are used in the calculation of demand forecasting.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-03-30 12 - 35 - 35
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 80871b4cacde2d37c2d044739b2cc7a2f8e9dfc6
ms.lasthandoff: 02/22/2017


---

# <a name="generate-a-statistical-baseline-forecast"></a>Generate a statistical baseline forecast

This article provides information about the parameters and filters that are used in the calculation of demand forecasting. 

When you create a baseline forecast, you must first specify the parameters and filters that are used in the calculation. For example, you can create a baseline forecast that estimates demand based on transaction data from the past year for a specific company, for the coming month, and for a selected group of items. To generate a demand forecast, go to **Master planning &gt; Forecasting &gt; Demand forecasting &gt; Generate statistical baseline forecast**. The forecast bucket can be selected at forecast generation time. The available values are: Day, Week, and Month. The number of buckets to generate a forecast for is set in the **Forecast horizon** field. When the forecast strategy is set to **Copy over historical demand**, the end of the historical horizon is ignored. The system copies the number of buckets specified in the **Forecast horizon** field to the forecast demand, starting from the date set in the **From date** field under **Historical horizon**. By copying historical demand from a certain date forward, production planners can make the plan for the next quarter in two ways:

-   By copying the demand from the same quarter last year.
-   By copying the demand from the previous quarter.

To prevent confusion in the production plans, a certain number of forecast buckets can be frozen. This number is set in the **Freeze time fence** field. On the **Adjusted demand forecast** page, the cells for the frozen buckets are disabled, to give a visual indication that those values should not be changed. The start date for the baseline demand forecast doesn’t have to be the current date or a date in the future. To set a different start date, use the **Baseline forecast start date - From date** field. For example, in June, users can generate a forecast for the next year. Because the forecast buckets between the end of historical demand and the start of the baseline are missing, the predictions might not be accurate. If you are using the Microsoft Dynamics 365 for Operations Demand forecasting service, there are four ways in which you can fill in the missing gaps. You can choose the method that you want by setting the MISSING\_VALUE\_SUBSTITUTION parameter on the **Demand forecasting parameters** page. The **Baseline forecast start date** - **From date** field has to be set to the beginning of a forecast bucket, for example, in the United States, a Sunday if the forecasting bucket is the week. The system automatically adjusts the **Baseline forecast start date** - **From date** field to match the beginning of a forecast bucket. The **Baseline forecast start date** - **From date** field can be set to a date in in the past. In other words, it is possible to generate a demand forecast in the past. This is useful, because it lets users tweak the forecast service parameters so that the statistical forecast generated in the past matches the actual historical demand. Users can then continue using these parameter settings to generate a statistical baseline forecast for the future. Manual adjustments made in previous demand forecasting iterations can be automatically applied to the new baseline forecast if the **Transfer manual adjustments to the demand forecas**t check box is selected. If the check box is cleared, the manual adjustments are not added to the baseline forecast – but they are not deleted. Manual adjustments made to a forecast can be deleted only at forecast import time, by clearing the **Save the manual adjustments made to the baseline demand forecast** check box. Manual adjustments are saved at authorization time. Therefore, if a user makes manual adjustments to the forecast, but doesn’t authorize the forecast back to Dynamics 365 for Operations, the changes are lost. For more information about manual adjustments and how they work, see [Authorizing the adjusted forecast](authorize-adjusted-forecast.md). A demand forecast generation can have a name and comments to help users identify the forecast that has been generated. These values are visible in forecast generation history on the **Statistical baseline forecast generation history** page. The intercompany planning group, item allocation keys, and other filters can be applied at forecast generation time. These can be used to improve performance or to split the data into manageable chunks. However, note that a demand forecast is not generated for the members of any item allocation key that is not associated with an intercompany planning group, even if the item allocation key is selected in the query. **Tip**: Sometimes users might receive errors while generating a demand forecast, or forecast generation is completed with no session log. This can happen because of leftover data in the query that was previously used for forecast generation. To fix this issue, click **Select** to open the **Query** page, click **Reset**, and then regenerate the baseline forecast. If the forecast is not generated for a big set of items, but, for example, for one item or one item allocation key at a time, then in order to get better performance, you can select the **Use request response mode** check box on the **Master planning - Setup - Demand forecasting** - **Demand forecasting parameters - Azure Machine Learning** tab.

<a name="see-also"></a>See also
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)


