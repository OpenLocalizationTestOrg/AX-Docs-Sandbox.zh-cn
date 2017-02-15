---
title: Import currency exchange rates | Microsoft Docs
description: "If a legal entity has received invoices in foreign currencies, it’s necessary to convert the foreign currency into the local currency. This means that up-to-date exchange rates for different currencies are required. This topic provides an overview of the required settings and processing for importing foreign exchange reference rates published over the Internet by the exchange rate providers, such as the European Central Bank and the Central Bank of Russia."
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-02 21:05:37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: 81
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 261374
ms.assetid: 0bcc76f8-3e6b-4ccd-a661-ef5a70488ad8
ms.region: Global
ms.author: epopov
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 68cf4dd15544a1c2fe15ec11aaf659a1f5e02298


---

# <a name="import-currency-exchange-rates"></a>Import currency exchange rates

If a legal entity has received invoices in foreign currencies, it’s necessary to convert the foreign currency into the local currency. This means that up-to-date exchange rates for different currencies are required. This topic provides an overview of the required settings and processing for importing foreign exchange reference rates published over the Internet by the exchange rate providers, such as the European Central Bank and the Central Bank of Russia.

The following sections describe the flow of information that is used for setting up and processing the import of foreign exchange rates.

## <a name="configure-an-exchange-rate-provider"></a>Configure an exchange rate provider
Before you can import exchange rates, you must set up the information that is required by the providers who offer the exchange rates. Use the **Configure exchange rate providers** page to select the exchange rate providers. Some exchange rate providers are included with the demo data in Microsoft Dynamics 365 for Operations. The following table provides descriptions for the controls on this page.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field** | **Description**                                                                                                                                                                                                             |
| **Name**  | The name of the exchange rate provider.                                                                                                                                                                                     |
| **Key**   | The unique identifier for each piece of configuration information that is required by the provider. This information is automatically added for each exchange rate provider that you add when you click the **Add** button. |
| **Value** | Information for each key. This information is added for each exchange rate provider that you add when you click the **Add** button.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Import currency exchange rates
You can import exchange rates from the exchange rate providers source, and set them up in the **Currency exchange rates** page. Use the **Import currency exchange rates** page to import the exchange rates. The following table provides descriptions the fields that are required to successfully complete the import process.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                              | **Description**                                                                                                                                                                                                                                                                                                                                                             |
| **Exchange rate type**                 | An exchange rate type.                                                                                                                                                                                                                                                                                                                                                      |
| **Exchange rate provider**             | An exchange rate provider.                                                                                                                                                                                                                                                                                                                                                  |
| **Import as of**                       | This parameter manages whether to import as of today’s date or for a date range. If you want to use a date range, enter or select starting and ending dates.                                                                                                                                                                                                                |
| **Create necessary currency pairs**    | This check box manages the automatic creation of currency pairs, if the currency pairs that are imported do not exist. This option might not be available for some providers.                                                                                                                                                                                               |
| **Override existing exchange rates**   | This check box manages the update of the existing exchange rate for a currency pair when the exchange rate for a specific date already exists. If you do not select this check box, the exchange rate for the specific dates is not imported if another exchange rate already exists.                                                                                       |
| **Prevent import on national holiday** | This check box manages the import of the exchange rate for a date that is a public holiday. For example, if you select this check box and use the European Central Bank as the exchange rate provider, the system will not update the exchange rate on a public holiday that is related to the current legal entity. This option might not be available for some providers. |






<!--HONumber=Feb17_HO3-->


