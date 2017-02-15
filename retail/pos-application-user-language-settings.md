---
title: POS application and user language settings | Microsoft Docs
description: This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.
author: josaw1
manager: AnnBe
ms.date: 2016-04-07 15:08:29
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: 41
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 78891
ms.assetid: 7d64a346-701c-46a5-ada8-6542a6058779
ms.region: global
ms.industry: Retail
ms.author: jeffbl
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: b9758363117ff8d8eec6e028114c6404dc7ef4f0


---

# <a name="pos-application-and-user-language-settings"></a>POS application and user language settings

This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.

<a name="overview"></a>Overview
========

Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings. For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.

## <a name="data-language"></a>Data language
Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data. This will ensure that all users and customers will have a consistent experience.  Examples of data include:

-   Products
-   Attributes and values
-   Category names
-   Printed or emailed transaction receipts
-   Payment method names
-   Line display messages

The store’s language will also be used for the main POS login screen, since the user is not known before logging in. If a translation is not available for the store’s language, the POS will revert to the company’s language.

### <a name="configuring-the-stores-language-setting"></a>Configuring the store’s language setting

The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language. **Use the drop down to choose the language for each store.

## <a name="user-interface-language"></a>User interface language
The POS user’s language setting determines the translations used in the application user interface. This includes all labels, menus, and lists that are not considered data. One exception is the text that is displayed on POS button grids. The button grids don't support translations, so they will always show the text as defined on the button. In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.

### <a name="configuring-the-users-language-setting"></a>Configuring the user’s language setting

The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.  It is not set on the main Profile tab.  This setting is not used by POS. If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **UI language** ** **      | **Data language (products, receipt formats, line display, etc.)** |
| **Company** | Default                    | Default                                                           |
| **Store**   | Overrides company          | Overrides company                                                 |
| **User**    | Overrides store or company | Never                                                             |






<!--HONumber=Feb17_HO3-->


