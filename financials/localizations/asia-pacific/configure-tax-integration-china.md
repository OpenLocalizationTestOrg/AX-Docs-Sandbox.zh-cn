---
title: Configure tax integration for China | Microsoft Docs
description: This topic describes the process for configuring tax integration for China.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-22 16:55:28
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 81
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 265264
ms.assetid: 25f99fbd-43e3-4e64-8ba5-2b1a6e45ec75
ms.region: China (PRC)
ms.author: leguo
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 6e47035f420c3597f9e6b8a171f0dd28aa2341d6


---

# <a name="configure-tax-integration-for-china"></a>Configure tax integration for China

This topic describes the process for configuring tax integration for China.

To configure tax integration for China, complete the following tasks.

1.  Create a new VAT invoice description on the **VAT invoice description** page. For example, you may need to set  the following parameters:
    -   **VAT invoice description ID** to InvoiceDescID01
    -   **Description** to 详见销售清单
    -   **Unit** to Box

2.  Create a new tax integration profile on the **Tax integration profiles** page. You can set up tax integration profiles to use when invoices are imported or exported. In the tax integration profile, you can specify the following:
    -   Sales tax code
    -   Maximum invoice amount
    -   Default description and unit for the golden tax invoice
    -   Whether to include non-deductible VAT invoices

The tax integration process is illustrated in the following diagram. [![IC666469](./media/ic666469.gif)](./media/ic666469.gif)

<a name="see-also"></a>See also
--------

[Import the Chinese Golden Tax data entity](https://docs.microsoft.com/en-us/dynamics365/operations/financials/localizations/asia-pacific/import-the-chinese-golden-tax-data-entity)




<!--HONumber=Feb17_HO3-->


