---
title: Address books | Microsoft Docs
description: 
author: kfend
manager: AnnBe
ms.date: 2015-12-11 23:25:59
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: DirPartyCheckDuplicate, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 23601
ms.assetid: bc23b9f7-d7e3-49ff-b782-c79efe3707f6
ms.region: Global
ms.author: kfend
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: ab766d6167ccbc2c9185b7caa2cd9d0cc25d33d4


---

# <a name="address-books"></a>Address books



<a name="how-do-i-check-for-duplicate-records"></a>How do I check for duplicate records?
-------------------------------------

You can check for duplicate records directly from the **Global address book** list page. On the Action Pane, on the **Party** tab, in the **Maintain** group, click **Check for duplicates**. Then select the values to include in the check for duplicates.

## <a name="can-i-bulk-add-or-delete-party-records-from-an-address-book"></a>Can I bulk add or delete party records from an address book?
Yes, you can add multiple party records to an address book and also remove multiple party records.

-   To add multiple party records to an address book, on the **Global address book** list page, select the parties in the list. Then, on the Action Pane, on the **Party** tab, in the **Maintain** group, click **Assign parties**. Select the address books to add the selected party records to, and then click **OK**. All the selected party records are added to the address books that you selected.
-   To remove multiple party records from an address book, on the **Global address book** list page, select the parties in the list. Then, on the Action Pane, on the **Party** tab, in the **Maintain** group, click **Remove parties**. Select the address books to remove the parties from, and then click **OK**. All the selected party records are removed from the address books that you selected.

## <a name="can-i-change-the-party-type-of-a-record-or-do-i-have-to-delete-the-old-record-and-create-a-new-one"></a>Can I change the party type of a record, or do I have to delete the old record and create a new one?
Occasionally, you might have to change the party type of a record from person to organization or from organization to person. For example, Nancy is a member of the sales team for Fabrikam U.K. At a trade show in London, she meets six new prospects. Nancy creates a prospect party record for each prospect. When Nancy saves the records, each record is also created in the global address book. Fabrikam has set the default party type to organization, but two of the new prospects should have a record type of person. Therefore, when Nancy returns from the trade show, she must change the party type of the two prospect records. To change a party record from one party type to another, you must first create a new party record of the correct type in the global address book. You then associate the old party record with this new record. After you have made the new party association, delete the original party record that has the incorrect record type.

## <a name="how-do-i-change-the-name-or-address-of-a-party-record"></a>How do I change the name or address of a party record?
You can update the name of a party record, and the addresses that are associated with that record, at any time.

-   To update the name of a party record, open the party record, and then, on the Action Pane, click **Edit**. On the **General** FastTab, enter the new name for the party, and then save the record.
-   To update an address for a party record, open the party record, and then, on the **Addresses** FastTab, select the address to update. Click **Edit**, and then, on the **Edit address** page, make the required changes to the address or address parameters.

## <a name="can-i-merge-two-or-more-party-records-into-one-record"></a>Can I merge two or more party records into one record?
Occasionally, you might want to merge two or more party records into a single record. This can occur if you create one or more duplicate party records, either on purpose or unintentionally. When you merge party records, you select one record to keep. The information from the other records is then merged into this record. For example, you discover that information about Fabrikam is stored in three party records: A, B, and C. You decide to keep party record A. Therefore, the information that is stored in party records B and C will be merged into party record A. There are some situations where you can't merge party records:

-   You can’t merge party records that are associated with the same party role, such as customer or vendor, in the same legal entity. For example, party A is associated with a customer in legal entity 123, and party B is associated with a different customer in legal entity 123. These party records can’t be merged, because if they were merged, the merged party record would be associated with multiple customers in the same legal entity, and this isn't allowed. However, the records can be merged if party B is associated with a vendor in legal entity 123 or with a customer in a different legal entity.
-   You can’t merge internal party organization records in the same legal entity, team, or operating unit.

## <a name="should-i-create-a-party-record-in-the-global-address-book-or-in-another-place-such-as-the-customer-or-vendor-page"></a>Should I create a party record in the global address book or in another place, such as the Customer or Vendor page?
You can enter party records either in the global address book or on the appropriate entity page. When you add a record in one location, the same record is always added in the other location. For example, if you add a party record for a customer in the global address book, the record is also added on the **Customer** page. Likewise, if you add a party record for a customer on the **Customer** page, the record is also added in the global address book. Use the following guidelines to decide where you should enter new party records:

-   **Creating a party record when you don't know the entity type** – If you must create a party record but don't know the entity type (for example, you don't know whether the entity is a customer or an opportunity), create the record in the global address book. You can select the entity type later.
-   **Creating a party record when you know the entity type** – If you know the entity type for the party, you can create a record on the applicable page for that type. For example, create a record for a customer on the **Customer** page. When you create and save a record by using the appropriate entity page, the record is automatically created in the global address book.

## <a name="can-i-translate-address-information-for-party-records"></a>Can I translate address information for party records?
You can set up translations of address information, so that the information appears in your user language (system language) in Microsoft Dynamics 365 for Operations but in another language on documents such as sales orders. You can enter translations for country/region names, address purposes, and name sequences. For example, your system language is Danish, and you create a sales order for a customer in France. In this case, you can view the customer record in Danish in the program but display the address information in French on the printed sales order. When you set up translations, you should enter a translation for every item in the list. Any item that you don't enter a translation for will appear in the system language. For example, your system language is Danish, and you send a document to a customer in Spain. If you haven't entered Spanish (ESP) translations for the address information, that information will appear in Danish both in the program and on the printed document.




<!--HONumber=Feb17_HO3-->


