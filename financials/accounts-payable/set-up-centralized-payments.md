---
title: Set up centralized payments
description: 
author: twheeloc
manager: AnnBe
ms.date: 2016-03-08 17 - 50 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 20ea9faa6671a119e663669e62b99d0175ec754c
ms.lasthandoff: 02/22/2017


---

# <a name="set-up-centralized-payments"></a>Set up centralized payments



Follow these steps to prepare to process payments in one legal entity on behalf of other legal entities in your organization. Before you begin, the following setup must be completed:

-   Create legal entities.
-   Set up General ledger parameters and charts of accounts.
-   Set up Accounts payable parameters and Accounts receivable parameters (depending on the modules that are using centralized payments).
-   Set up intercompany accounting.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Set up an organizational hierarchy for centralized payments
You must set up an organizational hierarchy for centralized payments. The same organizational hierarchy is used to process centralized vendor payments and centralized customer payments. **Note:** For centralized payments, the structure of the hierarchy doesn't matter. Any legal entity in the hierarchy will be able to process payments on behalf of any other legal entity in the hierarchy. On the **Organization hierarchies** page, you can create a new organization hierarchy.

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Set up an intercompany account for centralized payments
When payment transactions in the current legal entity are settled against invoices in other legal entities, the appropriate due-to and due-from transactions are created for each legal entity. You must specify the legal entity where any applicable cash discounts and realized gain or loss amounts are posted. Before you begin, decide which legal entity you will use to process vendor and customer payments. If one legal entity processes vendor payments but another legal entity processes customer payments, you will have to switch to each legal entity. On the **Intercompany accounting** page, you can select an intercompany relationship record for a legal entity that you will process payments on behalf of. On the **Centralized payments** tab, you can select whether to post cash discounts to the legal entity of the payment (or other transaction that decreases the balance of the vendor account) or the legal entity of the invoice (or other transaction that increases the balance of the vendor account). This selection works together with the **Cash discount administration** field on the **Accounts payable parameters** and **Accounts receivable parameters** pages. For overpayments and penny difference tolerances, the setting in the legal entity of the payment is used. For underpayments and penny difference tolerances, the setting in the legal entity of the invoice is used.

## <a name="map-vendor-accounts-across-legal-entities"></a>Map vendor accounts across legal entities
If you pay a vendor from one legal entity and want to select invoices for that vendor in other legal entities, you must make sure that all the corresponding vendor accounts in each legal entity use the same address book ID. If you receive a payment from a customer that pays invoices in more than one legal entity, you must make sure that all the corresponding customer accounts in each legal entity use the same address book ID.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Set up posting profiles for centralized payments
When you create a payment in one legal entity that settles invoices in other legal entities, the posting profile IDs must be the same in both legal entities. To help guarantee that payments are created correctly, in each legal entity of the invoice, set up a posting profile that corresponds to the posting profiles that are used in the legal entity of the payment. Switch to the first legal entity of the invoice, and then, on the **Vendor posting profiles** page, you can create a new posting profile or edit an existing posting profile. The selections that you make for the posting profile in the legal entity of the invoice don't have to match the setup of the posting profile in the legal entity of the payment.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Set up methods of payment for centralized payments
When you create a payment in one legal entity that settles invoices in other legal entities, the method of payment IDs must be the same in both legal entities. To help guarantee that payments are created correctly, in each legal entity of the invoice, set up a method of payment that corresponds to the methods of payment that are used in the legal entity of the payment. Switch to the first legal entity of the invoice, and then, on the **Methods of payment** page, you can create a new method of payment or edit an existing method of payment. The selections that you make for the method of payment in the legal entity of the invoice don't have to match the setup of the method of payment in the legal entity of the payment.

## <a name="set-up-default-descriptions"></a>Set up default descriptions
You can define default descriptions for intercompany settlement vouchers. The default description is included on the due-to and due-from transactions during the cross-company settlement process. On the **Default descriptions** page, you can create new descriptions for both **Intercompany customer settlement** and **Intercompany vendor settlement** by selecting a language and then entering text.


