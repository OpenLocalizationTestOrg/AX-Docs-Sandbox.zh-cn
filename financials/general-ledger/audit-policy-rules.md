---
title: Audit policy rules
description: You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create. All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.  Each policy rule is an instance of a policy rule type. For each policy rule type, only one policy rule can be active at a time.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-01 16 - 25 - 46
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: d1972efd3dec7d24ca7169680610732a030350bd
ms.lasthandoff: 02/22/2017


---

# <a name="audit-policy-rules"></a>Audit policy rules

You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create. All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.  Each policy rule is an instance of a policy rule type. For each policy rule type, only one policy rule can be active at a time. 

<a name="queries-and-query-types"></a>Queries and query types
-----------------------

When you create an audit policy rule, you first select a policy rule type. The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule. It also specifies the query type to use for the policy rule. The query determines the source document that the policy rule evaluates. It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit. The query type controls the default fields in the query page and in the Audit policy rule page. The following table shows the query types that are available for audit policy rules.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Query type</th>
<th>Purpose</th>
<th>More information</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Conditional</td>
<td>Evaluate source document attributes against specified values.</td>
<td></td>
</tr>
<tr class="even">
<td>Aggregate</td>
<td>Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</td>
<td></td>
</tr>
<tr class="odd">
<td>Sampling</td>
<td>Randomly select a specified percentage of the source documents to evaluate for policy violations.</td>
<td>When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</td>
</tr>
<tr class="even">
<td>Duplicate</td>
<td>Evaluate source documents to determine whether they contain duplicate entries in specified fields.</td>
<td>When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</td>
</tr>
<tr class="odd">
<td>List search</td>
<td>Evaluate source documents for specific entities.</td>
<td>The root document of the query defines the document that is being audited. The query must be a list query that includes a reference to the dirpartytable table. This option can be used only with the following AOT queries:
<ul>
<li><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</li>
<li><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</li>
</ul>
When you select this option, specify the monitored entities in the Audit policy rule page.</td>
</tr>
<tr class="even">
<td>Keyword search</td>
<td>Evaluate source documents to determine whether they contain certain words.</td>
<td>When you select this option, enter the words to look for in the Audit policy rule page. The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>Common parameters
All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range. These parameters are specified for the policy in the Additional options page.



<a name="see-also"></a>See also
--------

[Audit policy violations and cases](https://ax.help.dynamics.com/en/wiki/audit-policy-v…ns-and-cases-2/)


