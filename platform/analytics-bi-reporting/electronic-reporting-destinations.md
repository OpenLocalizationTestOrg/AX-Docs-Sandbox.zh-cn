---
title: Electronic reporting destinations
description: You can configure a destination for each Electronic reporting (ER) format configuration and its output component (a folder or a file). Users who are granted appropriate access rights can also modify destination settings at run time. This article explains ER destination management, the types of destinations that are supported, and security considerations.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-07-01 15 - 47 - 33
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.dyn365.ops.intro: 01-05-2016
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 4f8912456700e2cd9e9466fcc49fc036787ff3ca
ms.lasthandoff: 02/22/2017


---

# <a name="electronic-reporting-destinations"></a>Electronic reporting destinations

You can configure a destination for each Electronic reporting (ER) format configuration and its output component (a folder or a file). Users who are granted appropriate access rights can also modify destination settings at run time. This article explains ER destination management, the types of destinations that are supported, and security considerations.

Electronic reporting (ER) format configurations usually contain at least one output component: a file. Typically, configurations contain multiple file output components of different types (for example, XML, TXT, or XLSX) that are grouped into either a single folder or multiple folders. ER destination management lets you preconfigure what occurs when each component is run. By default, when a configuration is run, a dialog box appears that lets the user save or open the file. The same behavior is also used when you import an ER configuration and don't configure any specific destinations for it. After a destination is created for a main output component, that destination overrides the default behavior, and the folder or file is sent according to the destination's settings.

## <a name="availability-and-general-prerequisites"></a>Availability and general prerequisites
The ER destinations functionality isn't available in the Microsoft Dynamics AX 7.0 (February 2016) release. Therefore, you must install Microsoft Dynamics 365 for Operations (November 2016 release) to use all the functions that are described in this topic. Alternatively, you can install one of the following prerequisites. However, be aware that these alternative provide a more limited ER destination experience.

-   Microsoft Dynamics AX application version 7.0.1 (May 2016)
-   ER destination management [application hotfix](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

You can set up destinations only for ER configurations that have been imported, and for the formats that are available on the **Electronic reporting configurations** page.

## <a name="overview"></a>Overview
The ER destination management functionality is available at **Organization administration** &gt; **Electronic reporting**. Here, you can override the default behavior for a configuration. Imported configurations aren't shown here until you click **New** and then, in the **Reference** field, select a configuration to create destination settings for. \[caption id="attachment\_1657074" align="alignnone" width="640"\][![Selecting a configuration in the Reference field](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) ER destinations\[/caption\] After you've created a reference, you can create a file destination for each folder, or for a file. \[caption id="attachment\_1657084" align="alignnone" width="640"\][![Creating a file destination](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg) ER file destinations\[/caption\] **Note:** You can create one file destination for each output component of the same format, such as a folder or a file that is selected in the **File Name** field. You can then enable and disable individual destinations for the file destination in the **Destination settings** dialog box. The **Settings** button is used to control all the destinations for a selected file destination. In the **Destination settings** dialog box, you can control each destination separately by setting the **Enabled** option for it. \[caption id="attachment\_1657124" align="alignnone" width="640"\][![Destination settings dialog box](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg) ER destination settings\[/caption\]

## <a name="destination-types"></a>Destination types
Various types of destinations are supported. You can disable or enable all types at the same time. In this way, you can either do nothing or send the component to all configured destinations. The following sections describe the destinations that are supported.

### <a name="email-destination"></a>Email destination

Set **Enabled** to **Yes** to send an output file by email. After this option is enabled, you can specify the email recipients, and edit the subject and body of the email message. You can set up constant texts for the email subject and body, or you can use ER formulas to dynamically create email texts. You can configure email addresses for ER in two ways. The configuration can be completed in the same way that the Print management feature in Dynamics 365 for Operations completes it. Alternatively, you can resolve an email address by using a direct reference to the ER configuration through a formula.

### <a name="email-address-types"></a>Email address types

When you click **Edit** for the **To** or **Cc** field, the **Email to** dialog box appears. You can then select the type of email address to use. \[caption id="attachment\_1657134" align="alignnone" width="640"\][![Email to dialog box](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg) Selecting the email type\[/caption\]

#### <a name="print-management"></a>Print management

If you select the **Print Management email** type, you can enter fixed email addresses in the **To** field. To use email addresses that aren't fixed, you must select the email source type for a file destination. The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**. After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer **form. You can use this form to attach a formula that represents the selected party account to the email destination. \[caption id="attachment\_1657144" align="alignnone" width="640"\][![Configure print management email type](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) Print Management email type\[/caption\] Note that formulas are specific to the ER configuration. In the **Formula** field, enter a document-specific reference to a customer or vendor party type. Instead of typing, you can find the data source node that represents the customer or vendor account, and then click **Add data source** to update the formula. For example, if you use the ISO 20022 Credit Transfer configuration, the node that represents a vendor account is **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Otherwise, enter any string value, such as **DE-001**, to save a formula. \[caption id="attachment\_888993" align="alignnone" width="640"\][![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg) Destination formula designer – Vendor representation in the ISO 20022 Credit Transfer configuration\[/caption\] In the **Email to** dialog box, click the recycle bin next to the **Email source account** field to permanently delete the formula for the email source account. Alternatively, open the formula designer to change a formula that was previously saved. To assign email addresses, click **Edit** to open the **Assign email addresses** dialog box. \[caption id="attachment\_1657154" align="alignnone" width="640"\][![Assigning email addresses for an email destination](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg) Assigning email addresses for an email ER destination\[/caption\]

#### <a name="configuration-email"></a>Configuration email

Use this email type if the configuration that you use has a node in the data sources that represents an email address. You can use data sources and functions in the formula designer to get a correctly formatted email address. \[caption id="attachment\_1657164" align="alignnone" width="640"\][![Assigning an email address data source for an email destination](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) Assigning an email address data source for an email ER destination\[/caption\] **Note:** A Simple Mail Transfer Protocol (SMTP) server must be configured and available. You can specify your SMTP server in Dynamics 365 for Operations, at **System administration** &gt; **Setup** &gt; **Email** &gt; **Email parameters**.

### <a name="archive-destination"></a>Archive destination

You can use this option to send output to either a Microsoft SharePoint folder or Microsoft Azure Storage. Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type. Only document types where the group is set to **File** are available for selection. You define document types at **Organization administration** &gt; **Document management** &gt; **Document types**. The configuration for ER destinations is the same as the configuration for the document management system. \[caption id="attachment\_888823" align="alignnone" width="640"\][![Document types page](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) Document type – Group and location fields\[/caption\] The location determines where the file is saved. After the **Archive** destination is enabled, the results of configuration execution can be saved in the Job archive. You can view the results at **Organization administration** &gt; **Electronic reporting** &gt; **Electronic reporting archived jobs**. **Note:** You can select a document type for the Job archive in Dynamics 365 for Operations, at **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting** &gt; **Electronic reporting parameters**.

#### <a name="sharepoint"></a>SharePoint

You can save a file in a designated SharePoint folder. You define the default SharePoint server at **Organization administration** &gt; **Document management** &gt; **Document management parameters**, on the **SharePoint** tab. After the SharePoint folder is configured, you can select it as the folder where the ER output will be saved for the document type. \[caption id="attachment\_888833" align="alignnone" width="640"\][![Selecting a SharePoint folder](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) Document type – SharePoint folder selection\[/caption\]

#### <a name="azure-storage"></a>Azure Storage

When the document type location is set to **Archive directory**, you can save a file to Azure Storage.

### <a name="file-destination"></a>File destination

If you set **Enabled** to **Yes**, an open or save dialog box appears when the configuration has finished running.

### <a name="screen-destination"></a>Screen destination

If you set **Enabled** to **Yes**, a preview of the output is created. You can view some file types, such as XML, TXT, or PDF, directly in a browser window. For other file types, such Microsoft Excel or Word, the Microsoft Office Online service is used.

### <a name="power-bi-destination"></a>Power BI destination

Set **Enabled** to **Yes** to use your ER configuration to arrange the transfer of data from your instance of Dynamics 365 for Operations to Microsoft Power BI services. The transferred files are stored on a Microsoft SharePoint Server instance that must be configured for that purpose. For more information, see [Use an Electronic reporting configuration to provide Power BI with data from Dynamics 365 for Operations](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Hint:** To override the default behavior (that is, the dialog box for a configuration), you can create a destination reference and a file destination for the main output component, and then disable all the destinations.

## <a name="security-considerations"></a>Security considerations
Two types of privileges and duties are used for ER destinations. One type controls the ability to maintain the overall destinations that are configured for a legal entity (that is, it controls access to the **Electronic reporting destinations** page). The other type controls the ability of an application user to override, at run time, the destination settings that are configured by an ER developer or ER functional consultant.

| Role (AOT name)                     | Role name                                  | Duty (AOT name)                     | Duty name                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Electronic reporting developer             | ERFormatDestinationConfigure        | Configure electronic reporting format destination                |
| ERFunctionalConsultant              | Electronic reporting functional consultant | ERFormatDestinationConfigure        | Configure electronic reporting format destination                |
| PaymAccountsPayablePaymentsClerk    | Accounts payable payments clerk            | ERFormatDestinationRuntimeConfigure | Configure electronic reporting format destination during runtime |
| PaymAccountsReceivablePaymentsClerk | Accounts receivable payments clerk         | ERFormatDestinationRuntimeConfigure | Configure electronic reporting format destination during runtime |

**Note:** Two privileges are used in the preceding duties. These privileges have the same names as the corresponding duties: **ERFormatDestinationConfigure** and **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Frequently asked questions
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>I have imported electronic configurations, and I see them on the Electronic reporting configurations page. But why don't I see them on the Electronic reporting destinations page?

Make sure that you click **New** and then select a configuration in the **Reference** field. On the **Electronic reporting destinations** page, you can see only configurations that destinations have been configured for.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Is there any way to define which Azure Storage account and Azure Blob storage are used?

No. The default Azure Blob storage that is defined and used for the document management system is used.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>What is the purpose of the File destination in the destination settings? What does that setting do?

The **File** destination is used to control a dialog box. If you enable this destination, or if no destination is defined for a configuration, you see an open or save dialog box after an output file is created.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Can you give an example of the formula that refers to a vendor account that I can send email to?

The formula is specific to the ER configuration. For example, if you use the ISO 20022 Credit Transfer configuration, you can use **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** or **model.Payments.Creditor.Identification.SourceID** to get an associated vendor account.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>One of my format configurations contains multiple files that are group into one folder (for example, Folder1 contains File1, File2, and File3). How do I set up destinations so that Folder1.zip isn't created at all, File1 is sent by email, File2 is sent to SharePoint, and I can open File3 immediately after the configuration is run?

The prerequisite is that your format must be available in the ER configurations. If you have your format, open the **Electronic reporting destination** page, and create a new reference to this configuration. You must then have four file destinations, one for each output component. Create the first file destination, give it a name such as **Folder**, and select a file name that represents a folder in your configuration. Then click **Settings**, and make sure that all the destinations are disabled. For this file destination, the folder won't be created. By default, because of hierarchical dependencies between files and parent folders, the files will behave in the same way. In other words, they won't be sent anywhere. To override that default behavior, you must create three more file destinations, one for each file. In the destination settings for each, you must enable the destination that the file should be sent to.

<a name="see-also"></a>See also
--------

[Electronic reporting overview](general-electronic-reporting.md)


