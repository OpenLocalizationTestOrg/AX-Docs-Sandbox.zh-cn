---
title: SEPA direct debit overview
description: The Single Euro Payments Area (SEPA) is set up by the European Commission, and dictates that all electronic payments are considered domestic, regardless of the country/region where the individual, business, or organization, and the bank are located. There is no difference between national and cross-border payments. The SEPA includes the 28 European Union (EU) member states, as well as Iceland, Liechtenstein, Norway, Switzerland, Monaco and San Marino. The SEPA helps form a single market for payment transactions within the European Economic Area (EEA). Ultimately, the SEPA is expected to reduce the number of payment formats that banks, businesses, and individuals must work with.
author: twheeloc
manager: AnnBe
ms.date: 2015-10-28 22 - 23 - 07
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: mfalkner
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: a14e8b9ca930fe084a9b9e95fcb63f19fc9bdcbc
ms.lasthandoff: 02/22/2017


---

# <a name="sepa-direct-debit-overview"></a>SEPA direct debit overview

The Single Euro Payments Area (SEPA) is set up by the European Commission, and dictates that all electronic payments are considered domestic, regardless of the country/region where the individual, business, or organization, and the bank are located. There is no difference between national and cross-border payments. The SEPA includes the 28 European Union (EU) member states, as well as Iceland, Liechtenstein, Norway, Switzerland, Monaco and San Marino. The SEPA helps form a single market for payment transactions within the European Economic Area (EEA). Ultimately, the SEPA is expected to reduce the number of payment formats that banks, businesses, and individuals must work with.   

<a name="what-is-the-goal-of-sepa-direct-debits"></a>What is the goal of SEPA Direct Debits?
---------------------------------------

A SEPA Direct Debit allows a creditor to collect funds from a customer’s bank account, provided that a signed mandate has been granted by the customer to the creditor. The customer signs a mandate that authorizes the creditor to collect a payment and instructs the customer’s bank to pay the collection. SEPA Direct Debits create, for the first time, a payment instrument that can be used for both national and cross-border euro direct debits throughout the 32 SEPA countries/regions. There are two schemes available: the SEPA Core Direct Debit Scheme and the SEPA Business to Business (B2B) Direct Debit Scheme. Both schemes use the same file format.

## <a name="what-is-the-core-direct-debit-scheme"></a>What is the Core Direct Debit scheme?
The SEPA Core Direct Debit Scheme is the basic scheme. It has the following attributes:
-   The transfer of funds is in euros (even though the bank accounts may hold funds in other currencies).
-   The customer and creditor must each hold an account with a credit institution that is located within the SEPA.
-   The customer must grant a signed mandate to the creditor.
-   Mandates expire 36 months after the last initiated collection.
-   The creditor must store mandates for as long as the mandate is valid and for at least 14 months after the last collection.
-   The scheme may be used for single (one-time) or recurring direct debit collections.
-   Customers have a “no questions asked” right to receive a refund for up to eight weeks after the debit of their account.

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a>What is the SEPA Business to Business (B2B) Direct Debit scheme?
The SEPA B2B Direct Debit Scheme applies to business-to-business transactions and builds on the SEPA Core Direct Debit Scheme. The main differences are:
-   The SEPA B2B Direct Debit Scheme is not allowed when the customer is a private individual (consumer).
-   The customer is not entitled to obtain a refund of an authorized transaction.
-   Customer banks must make sure that that the collection is authorized, by verifying the collection against mandate information. Customer banks and customers are required to agree on the verification that will be performed for each direct debit.
-   The scheme offers a shorter timeline for presenting direct debits and reduces the return period.

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a>Can I use the COR1 scheme for direct debit mandates?
Yes. You can use the COR1 scheme for SEPA direct debit mandates in Austria, Belgium, Germany, France, Italy, Spain, and the Netherlands. The scheme provides a shorter pre-notification period for the direct debit collection for the creditor.

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a>What are International Bank Account Numbers (IBAN) and Bank Identifier Codes (BIC)?
The International Bank Account Number (IBAN) and Bank Identifier Code (BIC) are used to identify any account in the 32 SEPA countries/regions. Enter the BIC in the SWIFT code field and the IBAN in the IBAN field. Both fields are located on the Additional identification FastTab on the Bank account tab in the Bank accounts page. This is true for both the creditor’s bank account and the customer’s bank account.

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a>Where do I enter creditor identifiers (Direct debit IDs)?
In the SEPA, each creditor is identified by a unique creditor identifier. This identifier lets the customer and the customer bank filter each direct debit, and then process or reject the direct debit according to customer instructions. Creditors must request this identifier through their bank. Enter this identifier in the Direct debit ID field for the bank account for the legal entity.

## <a name="what-are-mandates"></a>What are mandates?
The customer signs a mandate that authorizes the creditor to collect a payment and instructs the customer’s bank to pay the collection. The customer can issue the mandate in paper form or electronically. By default, the mandate expires 36 months after the direct debit is last initiated.

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a>Where do I specify the SEPA Direct Debit file format (ISO 20022)?
The SEPA data formats are based on the ISO 20022 message standards. You will check the Generic electronic reporting checkbox and select the SEPA Direct debit format as an export format configuration when you configure accounts receivable methods of payment. You use that method of payment when you generate a payment file in a customer payment journal.

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a>In what file formats can I generate SEPA direct debit payment files?
You can generate electronic payment files for SEPA direct debits in the following formats:
-   SEPA direct debit payment files in the PAIN.008.001.02 XML file format for Belgium, Germany, Spain, France, Italy, and the Netherlands.
-   SEPA direct debit payment files in the PAIN.008.001.02 XML file format for Austria, and in the PAIN.008.003.02 XML file format for Germany.

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a>How do refunds and returns work with SEPA direct debits?
Under both SEPA Direct Debit schemes, customers have certain rights to refunds. The customer is allowed to recall any authorized transactions during an eight-week period after the due date, without having to give a reason. In the case of unauthorized transactions, the period is extended to 13 months after the due date. Reversals of any payments that have been made are accomplished manually by using the Cancel payment button in the Customer transactions page.




