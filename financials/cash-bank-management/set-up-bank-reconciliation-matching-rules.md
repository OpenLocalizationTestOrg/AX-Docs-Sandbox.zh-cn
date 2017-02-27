---
title: Set up bank reconciliation matching rules
description: This article explains how to set up reconciliation matching rules and reconciliation matching rule sets to help with the bank reconciliation process. Reconciliation matching rules are a set of criteria that are used to filter bank statement lines and bank document lines during the reconciliation process.
author: ShylaThompson
manager: AnnBe
ms.date: 2015-12-01 16 - 05 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 6a9fa4e110c73cbf4397adc943f74606f144c642
ms.lasthandoff: 02/22/2017


---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Set up bank reconciliation matching rules

This article explains how to set up reconciliation matching rules and reconciliation matching rule sets to help with the bank reconciliation process. Reconciliation matching rules are a set of criteria that are used to filter bank statement lines and bank document lines during the reconciliation process.

You can set up reconciliation matching rules and reconciliation matching rule sets to help with the bank reconciliation process. A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Operations bank transaction lines during the reconciliation process. Use the **Reconciliation matching rules** page to set up the reconciliation matching rules. You can set up more than one matching rule and then create a reconciliation matching rule set on the **Reconciliation matching rule sets** page. **Note:** Bank reconciliation matching rules are used if you reconcile an electronic bank statement by using advance bank reconciliation. On the **Reconciliation matching rules** page, you can select which actions and selection criteria are used when the matching rule is run. In the **Actions** field group, select the action that will be performed when the matching rule is run during the reconciliation process.  **Note:** The option that you select determines the fields that appear.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Action**                         |                                                                                                                                                                                                                                                                                                               | **Selection criteria available when action is selected**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Match with bank document**       | Create criteria to specify how the bank documents and bank statement lines are matched when the matching rule is run from the **Bank reconciliation worksheet** page. The transaction lines are selected according to the additional criteria that are set up on the FastTabs.                                | **Step 1: Define the matching rule** – Select criterias to specify which bank statements should be matched with Dynamics 365 for Operations bank transactions. **Step 2 (optional) : Select the statement lines to run matching rules against:**  Apply a filter on which statement line to run the rules against.                                                                                                                                                                                                                                                                                                               |
| **Clear reversal statement lines** | Create criteria to specify how reversal statement lines should be removed from the **Bank reconciliation worksheet** page when the matching rule is run. This option is used when a bank error causes two bank statement lines to be listed in the imported bank statement, and the lines must be reconciled. | **Step 1**: **Find reversal statement lines** – Add selection criteria to select reversal bank statement lines. For example, to select only checks, select the **Bank transaction code** in the Field field, select the plus sign (+) in the **Operator** field, and then enter **Checks** in the Value field. **Step 2: Find original statement lines** – You can add selection criteria to match bank document lines to bank statement lines. **Step 3: Find Dynamics  365 for Operations bank transactions **– You can add selection criteria to match Dynamics 365 for Operations bank transactions to bank statement lines. |
| **Mark new transactions**          | Create criteria to specify how new transactions should be marked on the **Bank reconciliation workshee**t page when the matching rule is run.                                                                                                                                                                 | **Step 1: Find statement lines** – Add selection fields to specify which bank statement lines should be selected from the **Bank reconciliation worksheet** page. **Step 2: Find Dynamics 365 for Operations bank transactions **– You can add selection criteria to search bank document lines. If no bank document is found, a statement line will be marked as a new transaction.                                                                                                                                                                                                                                             |

 

### 

<a name="see-also"></a>See also
--------

[Advanced bank reconciliation overview](https://ax.help.dynamics.com/en/wp-admin/post.php?post=256174&action=edit)


