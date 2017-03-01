---
title: Toolbar and Fields subpattern
description: This article provides information about the Toolbar and Fields subpattern. This container pattern is used to show actions above a subpattern of data fields. The toolbar should contain fewer than 10 actions.
author: jasongre
manager: AnnBe
ms.date: 2015-12-03 21 - 26 - 28
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations
ms.custom: 15911
ms.assetid: c5d6aa38-1f5f-41e5-9d90-11766d34a947
ms.search.region: Global
ms.author: jasongre
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: a63d6f51e42e0b98919782bec873a75c3d7f88ac
ms.lasthandoff: 02/22/2017


---

# <a name="toolbar-and-fields-subpattern"></a>Toolbar and Fields subpattern

This article provides information about the Toolbar and Fields subpattern. This container pattern is used to show actions above a subpattern of data fields. The toolbar should contain fewer than 10 actions.

<a name="usage"></a>Usage
-----

This container pattern is used to show actions above a subpattern of data fields. The toolbar should contain fewer than 10 actions.

## <a name="wireframe"></a>Wireframe
[![ToolbarFields(1)](./media/toolbarfields1.png)](./media/toolbarfields1.png)

## <a name="model"></a>Model
### <a name="high-level-structure"></a>High-level structure

\[Container\]

Toolbar (ActionPane, Style=Strip)

ContentGroup (Group) – **Note:** A fields subpattern is used.

### <a name="core-components"></a>Core components

-   Apply the ToolbarFields subpattern to the container control.
-   Address BP Warnings:
    -   No additional BP checks are required beyond the AX6.3 BP checks that were carried forward.

### <a name="related-patterns"></a>Related patterns

-   [Toolbar and List](toolbar-list-subpattern.md)

### <a name="commonly-used-subpatterns"></a>Commonly used subpatterns

-   [Fields and Field Groups](fields-field-groups-subpattern.md)
-   [Tabular Fields](tabular-fields-subpattern.md)
-   [Dimension Expression Builder](dimension-expression-builder-subpattern.md)

## <a name="ux-guidelines"></a>UX guidelines
The verification checklist shows the steps for manually verifying that the form complies with UX guidelines. This checklist doesn't include any guidelines that will be enforced automatically through the development environment. Open the form in the browser, and walk through these steps. **Standard form guidelines:**

-   Standard form guidelines have been consolidated into the Microsoft Dynamics AX [General Form Guidelines](general-form-guidelines.md)document.

**Toolbar** **guidelines:**

-   Toolbar guidelines have been consolidated into the Dynamics AX [General Form Guidelines ](general-form-guidelines.md)document.

## <a name="examples"></a>Examples
### <a name="toolbar-and-fields"></a>Toolbar and Fields

Form: **HcmPosition** **(WorkerAssignmentTabPage)** [![ToolbarFields(2)](./media/toolbarfields2-1024x131.png)](./media/toolbarfields2.png)

## <a name="resources"></a>Resources
### <a name="typically-used-by-patterns"></a>Typically used by patterns

-   [Simple List and Details](simple-list-details-form-pattern.md)
-   [Table of Contents](table-of-contents-form-pattern.md)
-   [Details Master](details-master-form-pattern.md)
-   [Details Transaction](details-transaction-form-pattern.md)

## <a name="appendix"></a>Appendix
### <a name="frequently-asked-questions"></a>Frequently asked questions

This section will have answers to frequently asked questions that are related to this guideline/pattern.

### <a name="open-issues"></a>Open issues

-   **Should the ShowMoreLess group be part of the pattern, or should it be its own subpattern?**
    -   We will treat the **ShowMoreLess** group as a custom container pattern until there is enough demand to justify the addition of a new pattern.

### <a name="microsoft-dynamics-ax-2012-content"></a>Microsoft Dynamics AX 2012 content

**HcmPosition** ![ToolbarFields(3)](./media/toolbarfields3.png)


