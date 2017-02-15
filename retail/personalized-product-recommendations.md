---
title: Personalized product recommendations overview | Microsoft Docs
description: "In Dynamics 365 for Operations, product recommendations can be displayed on the point of sale (POS) device. The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores. For retailers with large catalogs, recommendations help the customer with product discovery. By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention. In Dynamics 365 for Operations, product recommendations are powered by cognitive services and Microsoft Azure machine learning."
author: josaw1
manager: AnnBe
ms.date: 2016-11-28 23:43:23
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 41
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 259664
ms.assetid: f26f75b2-2538-4753-8925-2347701cb060
ms.region: global
ms.industry: Retail
ms.author: asharchw
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 209878d3c342bf3e54fa090ebacac2014aef827a


---

# <a name="personalized-product-recommendations-overview"></a>Personalized product recommendations overview

In Dynamics 365 for Operations, product recommendations can be displayed on the point of sale (POS) device. The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores. For retailers with large catalogs, recommendations help the customer with product discovery. By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention. In Dynamics 365 for Operations, product recommendations are powered by cognitive services and Microsoft Azure machine learning.

<a name="scenarios"></a>Scenarios
---------

Product recommendations are enabled for the following POS scenarios. They are available in Cloud POS or Modern POS (MPOS).

1.  On the **Product details** page:

-   If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.
-   If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

1.  On the **Transaction** page:

-   The recommendation engine suggests items based on the entire list of items in the basket.
-   If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.

**Note**  To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Operations. The **Recommendations** control must be dropped on to the **Transaction** page. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

1.  On the **Customer details** page:
    -   The recommendation engine suggests items based on the user ID and items in the customer’s wish list.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Configure Dynamics 365 for Operations to enable POS recommendations
To set up product recommendations, you need to do the following.

1.  Make sure that you have selected the correct **Legal entity**.
2.  Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.** **This will use the demo data (or your data) from your operational database and move it to Entity store.
3.  Optional: To display recommendations on the transaction screen, go to **Screen Layout, **choose your screen layout, launch the **Screen layout designer**,** **and then drop the **recommendations control **where needed.
4.  Go to **Retail parameters**, select **Machine-learning**, select **Yes **under **Enable POS recommendations**.
5.  To see recommendations on POS, run global configuration job **1110**. To reflect changes made to POS screen layout designer, run channel configuration job **1070**.

## <a name="how-does-it-work"></a>[]()How does it work?
When you refresh the **Entity store** entity, the following actions take place.

-   Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Operations operational database and sent to the Entity store.
-   The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities. Cleansed data is stored in blob storage.
-   Data from blob storage is used by the Cognitive services API to train a recommendation model.

When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.

-   Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Operations operational database, in the web.config for AOS, and also in the retail server.
-   Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.


<a name="see-also"></a>See also
--------

[Add a recommendations control to the transaction page on a POS device](https://docs.microsoft.com/en-us/dynamics365/operations/retail/add-recommendations-control-to-the-transaction-screen-on-pos-using-screen-layout-designer)




<!--HONumber=Feb17_HO3-->


