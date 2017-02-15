---
title: Action search | Microsoft Docs
description: This article describes the action search functionality in Microsoft Dynamics 365 for Operations. Action search will help you find and run actions on a page.
author: jasongre
manager: AnnBe
ms.date: 2016-03-08 19:35:39
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 71
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 62303
ms.assetid: 3d7dfcaa-4be2-4fdc-ac35-cc96868f56ab
ms.region: Global
ms.author: jasongre
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: dbe55db0848a0b2f55ecdd7d08c9be9436dcf7ca


---

# <a name="action-search"></a>Action search

This article describes the action search functionality in Microsoft Dynamics 365 for Operations. Action search will help you find and run actions on a page.

<a name="introduction"></a>Introduction
------------

Pages in Microsoft Dynamics 365 for Operations primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page. In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters. [![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) However, in the current version of Dynamics 365 for Operations, Key Tips are no longer available but have been replaced by the action search feature. This new feature lets you quickly search for and run a button from any visible Action Pane.

## <a name="using-action-search"></a>Using action search
To use the action search feature, follow these steps.

1.  On the Action Pane, click in the **action search** field. (The **action search** field contains a magnifying glass icon.)
2.  Type all or part of the name of the button that you want to run. You can also search by using words from the button's "path." (For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.
3.  Find and run the button in the results list (by using your mouse or keyboard).

After the button is run, the focus is returned to your last position on the page, so that you can continue to work. [![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)

You can also start action search by pressing Ctrl+/ or Alt+Q. Press the keyboard shortcut again to return the focus to your last position on the page.

## <a name="understanding-the-results-list"></a>Understanding the results list
Often, in Dynamics 365 for Operations, you must know both the location and the context of a button to fully understand the purpose of that button. Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list. In particular, the "path" of the button is shown. This path might include the labels of the following UI elements, as relevant:

-   Action Pane tab
-   Button group
-   Menu button (if the button is inside a menu button)
-   Menu separator (if the button is inside a named group inside a menu button)
-   Group or tab on the page (for example, the name of a FastTab)

For example, you typed **tot** in the **action search** field and are now examining the results list. The first entry, for a button that is named **Totals**, is highlighted. A button path of **Sales order** &gt; **View** is also shown. The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane. Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list). [![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) In the previous example, action search showed results from the standard Action Pane at the top of a page. However, action search also shows results from visible toolbars that are located in other places on the page. For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab. In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab. [![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Action search vs. Navigation search
Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages in Dynamics 365 for Operations. For more information about that feature, see the [Navigation search](https://docs.microsoft.com/en-us/dynamics365/operations/core/get-started/navigation-search-feature) article.




<!--HONumber=Feb17_HO3-->


