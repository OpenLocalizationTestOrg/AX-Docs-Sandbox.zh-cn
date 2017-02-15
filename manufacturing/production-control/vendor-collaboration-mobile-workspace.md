---
title: Vendor collaboration mobile workspace for Microsoft Dynamics 365 for Operations app | Microsoft Docs
description: With the vendor collaboration mobile workspace, your vendors can stay up-to-date on the purchase orders that have been sent to them for approval and view information about new and updated purchase orders and contacts.
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16:36:37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 121
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 267074
ms.assetid: eb111191-b7cd-48df-ba18-769f8b8ffb8d
ms.region: global
ms.author: mkirknel
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 95ef4932854637ef7a91e286befa5929126d158d


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Vendor collaboration mobile workspace for Microsoft Dynamics 365 for Operations app

With the vendor collaboration mobile workspace, your vendors can stay up-to-date on the purchase orders that have been sent to them for approval and view information about new and updated purchase orders and contacts.

<a name="prerequisites"></a>Prerequisites
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prerequisite</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Read about the Microsoft Dynamics 365 for Operations mobile platform</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/mobile-development-handbook">Dynamics 365 for Operations mobile platform</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>Be sure that you’re using an environment that has Microsoft Dynamics 365 for Operations version 1611 and Microsoft Dynamics for Operations platform update 3 (November 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Mobile device that has the Dynamics 365 for Operations app installed</span></td>
<td><span style="color: #000000;">Download the Dynamics 365 for Operations app from your mobile app store.</span></td>
</tr>
<tr class="even">
<td>Hotfix KB 3215650</td>
<td>Install the hotfix to enable the workspaces that are provided in Dynamics 365 for Operations.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Hotfix KB 3216943</span> </span></td>
<td>Install the hotfix to enable the vendor collaboration mobile workspace.</td>
</tr>
<tr class="even">
<td>The vendor user must have access to the vendor collaboration web interface in Dynamics 365 for Operations and set up a vendor collaboration user.</td>
<td>Follow the steps described in the following topics to set up and work with the vendor collaboration web interface.
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/procurement-sourcing/using-vendor-collaboration-to-work-with-external-vendors">Use vendor collaboration to work with external vendors</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/core/organization-administration/manage-vendor-collaboration-users">Manage vendor collaboration users</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/core/organization-administration/set-up-and-maintain-vendor-collaboration">Set up and maintain vendor collaboration</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/procurement-sourcing/using-vendor-collaboration-to-work-with-customers-in-dynamics-365-for-operations">Use vendor collaboration to work with customers in Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Overview
The Vendor collaboration mobile workspace keeps vendors informed about new purchase orders so that they can see and respond to purchase orders in the Dynamics 365 for Operations web client. **Note:** The mobile workspace should be used as a supplement to the vendor collaboration web interface, but not a replacement. With the Vendor collaboration mobile workspace, your vendors can view new purchase orders that are sent for approval. It displays purchase order information, such as products, quantity, and requested delivery dates. Price information is available, depending on the configuration for each vendor. When a user logs in as a vendor, they will see which purchase orders have been responded to, or which purchase orders are still awaiting customer action. The vendor might have suggested another delivery date that is not yet agreed with the customer so the purchase order is awaiting customer action. The vendor will also see a list of purchase orders that are confirmed but not yet delivered. To respond to a purchase order, the vendor has to use the vendor collaboration web interface that is available in the Dynamics 365 for Operations web client. This is also where the vendor will get more information about the order, such as document attachments, delivery address per line, and charges that are associated with the vendor. With a special security role, the vendor can view which contact persons are registered for a vendor account. With the same security role, the vendor can view the status of any user request that has been submitted. Creating new contacts and submitting new user requests must be done in the vendor collaboration interface that is available in the Dynamics 365 for Operations web client. With the mobile workspace, your vendor can:

-   View new purchase orders sent to the vendor.
-   View purchase orders that the vendor has responded to and are awaiting customer action.
-   View purchase orders that are in a confirmed state and have not been fully received.
-   View contact person information that is registered for the vendor account (requires an additional security role).
-   View information and follow the status of a user request submitted by the vendor (requires an additional security role).

## <a name="get-started"></a>Get started
To get started on your mobile device:

1.  On your mobile app store, download and install the Microsoft Dynamics 365 for Operations app.
2.  Start the app on your device.
3.  Enter your Dynamics 365 URL.
4.  Enter the company to sign in to. For example, enter **USMF**.
5.  The first time that you sign in, you’re prompted for the user name and password for your Microsoft Dynamics 365 for Operations account. 

After you log in the app, no workspaces are visible. To view workspaces on your mobile app, you must first publish the desired workspaces to the Dynamics 365 for Operations app. You need system administration permission to publish the workspace.

1.  Start Dynamics 365 for Operations.
2.  Go to **System administration** &gt; **Setup** &gt; **system parameters**.
3.  Select **Manage mobile app**.
4.  Select the workspace **Vendor collaboration** to publish to the mobile platform.
5.  Select **Publish workspace**.
6.  Refresh your device to see the published workspaces.
7.  Select the **Vendor collaboration** workspace. You will the following page.

[![vendor-collaboration-mobile-app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Contacts
The **Contacts** page lets you see all the contacts that have been set up for the vendor account. It shows the contact person name, primary email, and the users alias, if available. It also shows whether the contact person's user account is active. When you select a contact, you see contact details, such as which legal entities the person is a contact for, and contact information such as phone number or a different email address.

## <a name="user-requests"></a>User requests
The **User requests** page lets you see all the user requests that you have submitted via the vendor collaboration web interface and follow the status. When you select a user request, you can see what was requested, add or inactivate a user, change security, and see which security roles were requested for the user.

## <a name="purchase-orders-ready-for-review"></a>Purchase orders ready for review
The **Purchase orders ready for review** page lets you see all the purchase orders that were sent by the customer and have not been answered. You can view selected information about the order, such as which products have been requested and when to deliver. Price information is only available if this is configured for the vendor. You can see whether the purchase order has notes or attachments. To open attachments, you need to use vendor collaboration in the web client. Select **Purchase order line** to see all the lines with details. Note that for each line, an indicator will show whether there are notes or attachments or if there's a delivery address that's different than what's shown on the header. To respond to the purchase order, you must use the vendor collaboration web client.

## <a name="awaiting-customer-action"></a>Awaiting customer action
The **Awaiting customer action** page lets you find purchase orders that you, or someone in your company who also has access to vendor collaboration, have responded to. The purchase orders are only visible in this list if the customer needs to perform one of the following actions on the purchase order.

-   If the purchase order was rejected, the customer would either need to update the sent order and send again, or cancel the order and resend. When the purchase order is sent again, it will disappear from the **Awaiting customer action** page.
-   If the purchase order was accepted with changes, the customer would need to update the original order and resend for review, or update it according to the changes and confirm it immediately. In both cases, the purchase order will disappear from the **Awaiting customer action** page.
-   If the purchase order was accepted and appears in the **Awaiting customer action** page, it is because the purchase order was not automatically confirmed when the acceptance was done. It is waiting for a purchasing agent to change the order to Confirmed. Typically, the purchase order would be regarded as an agreement between the customer and vendor as soon as the vendor accepts the order. Moving the purchase order to the Confirmed state would be a formality.

By selecting the purchase order, additional details appear about the response. You can see the line details and response for every line. The line status shows which of the following responses has been given.

-   Accepted
-   Rejected
-   Accepted with changes
-   Substituted/Substitute
-   Split into schedule/Schedule line

Note that an indicator shows **Delivering**=yes/no, which is used to indicate that the lines will not be delivered. This could be because the line was rejected, or substituted where the original lines are not expected to be delivered, or a line that has been split into multiple schedule lines and the original line is not expected to be delivered as requested in the received order. Any changes made to the order line response are displayed, except for the uploaded notes and attachments, which you can see by using the vendor collaboration web interface.

## <a name="open-confirmed-orders"></a>Open confirmed orders
When the purchase order is confirmed by the customer, which means the purchase order is changed to the Confirmed state, it will appear in the open confirmed order. It will stay in the list until it is registered as received by the customer.




<!--HONumber=Feb17_HO3-->


