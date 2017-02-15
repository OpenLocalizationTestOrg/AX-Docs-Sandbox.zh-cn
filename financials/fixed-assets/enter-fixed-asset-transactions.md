---
title: Fixed asset transaction options | Microsoft Docs
description: This article describes the different methods available to create fixed asset transactions.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-11 22:58:38
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 23061
ms.assetid: eec29cba-f5c3-4f0f-960b-bb3ed9baff86
ms.region: Global
ms.author: saraschi
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 91863f16f3bb253bf1af7b65edf143a2b8bd2f6d


---

# <a name="fixed-asset-transaction-options"></a>Fixed asset transaction options

This article describes the different methods available to create fixed asset transactions.

You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger. You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.

## <a name="accounts-payable"></a>Accounts payable
You can enter Fixed assets transactions in the Journal voucher page. This page can be opened from the Invoice journal page. You can also open the Journal voucher page from the Invoice approval journal page. In the Offset account type field, select Fixed assets. Then, in the Offset account field, select a fixed asset number. On the Fixed assets tab, enter values in the Transaction type and Book fields.

## <a name="accounts-receivable"></a>Accounts receivable
You can enter Fixed assets transactions in the Free text invoice page.  In the Free text invoice page, in the Invoice lines grid, select a line item. Click the Line details FastTab. Enter the fixed asset number and book for the disposal transaction. For free text invoices, the fixed asset transaction type is always Disposal - sale.

## <a name="procurement-and-sourcing"></a>Procurement and sourcing
You can enter Fixed assets transactions in the Purchase order page. Enter the required information to create a purchase order, and then click OK. In the Purchase order page, click the Line details FastTab. Then, on the Fixed assets tab, enter information about the fixed asset. To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type. The fixed asset cannot be posted if any of this information is missing. To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to. However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model. Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules. When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.

## <a name="general-ledger"></a>General ledger
Any fixed asset transaction type can be posted in the General journal page. You can also use journals in Fixed assets to post fixed asset transactions.

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Options for entering fixed asset transaction types
### 

| Transaction type                    | Module                   | Options                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Acquisition, Acquisition adjustment | Fixed assets             | Fixed assets, Inventory to fixed assets   |
|                                     | General ledger           | General journal                           |
|                                     | Accounts payable         | Invoice journal, Invoice approval journal |
|                                     | Procurement and sourcing | Purchase order                            |
| Depreciation                        | Fixed assets             | Fixed assets                              |
|                                     | General ledger           | General journal                           |
| Disposal                            | Fixed assets             | Fixed assets                              |
| ** **                               | General ledger           | General journal                           |
| ** **                               | Accounts receivable      | Free text invoice                         |



<a name="see-also"></a>See also
--------

[Fixed assets integration](https://docs.microsoft.com/en-us/dynamics365/operations/financials/fixed-assets/fixed-assets-integration)




<!--HONumber=Feb17_HO3-->


