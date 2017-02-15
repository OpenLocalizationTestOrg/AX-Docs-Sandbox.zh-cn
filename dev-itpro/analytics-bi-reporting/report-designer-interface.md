---
title: Report Designer interface | Microsoft Docs
description: This article explains how to navigate through Report Designer and how to use the various options to meet your specific requirements.
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 18:50:10
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.suite: Released- Dynamics AX application 7.0.1
ms.custom: 59041
ms.assetid: a67b4c9d-28c6-442b-b0c1-bd5a88999f8f
ms.region: Global
ms.author: aolson
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 6fae541a5fe28747eb1943fc42a97b8aafabc5fe


---

# <a name="report-designer-interface"></a>Report Designer interface

This article explains how to navigate through Report Designer and how to use the various options to meet your specific requirements. 

<a name="report-designer-menu-commands"></a>Report Designer menu commands
-----------------------------

The following tables describe the menu commands and options that you can use when you design financial reports. Some menu commands and options are available only in specific circumstances. For example, the commands for promoting and demoting reporting units are available only when you're modifying a reporting tree definition.

### <a name="file-menu"></a>File menu

The **File** menu is available to all users and includes the following commands.

| Command                           | Description                                                                                                                                                                                      |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| New                               | Create a new report definition, row definition, column definition, reporting tree definition, report group definition, or folder. Additional options are available, depending on your user role. |
| Open                              | Open an existing row definition, column definition, reporting tree definition, or report definition.                                                                                             |
| Close                             | Close the current building block.                                                                                                                                                                |
| Close All                         | Close all building blocks.                                                                                                                                                                       |
| Save                              | Save the current row definition, column definition, reporting tree definition, or report definition.                                                                                             |
| Save As                           | Save the current row definition, column definition, reporting tree definition, or report definition under a new name.                                                                            |
| Properties                        | Open the **Properties** dialog box, where you can change the name and description of a report.                                                                                                   |
| Generate                          | Generate the current report. This command is available from a report definition.                                                                                                                 |
| View Report                       | Open the most recent version of the generated report in Dynamics AX. This command is available from a report definition if you've generated at least one report.                                 |
| Recent Report Definitions         | Show a list of reports that have recently been created or modified. You can then select a report in the list.                                                                                    |
| Recent Row Definitions            | Show a list of row definitions that have recently been created or modified. You can then select a row definition in the list.                                                                    |
| Recent Column Definitions         | Show a list of column definitions that have recently been created or modified. You can then select a column definition in the list.                                                              |
| Recent Reporting Tree Definitions | Show a list of reporting tree definitions that have recently been created or modified. You can then select a reporting tree definition in the list.                                              |
| Exit                              | Exit Report Designer.                                                                                                                                                                            |

### <a name="edit-menu"></a>Edit menu

The **Edit** menu is available to users who have the **Designer** or **Administrator** role. This menu includes the following commands.

| Command                                | Description                                                                                                                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Undo                                   | Undo the last action.                                                                                                                                                                                              |
| Redo                                   | Reverse the last undo action.                                                                                                                                                                                      |
| Cut                                    | Delete the selected text, and copy it to the clipboard.                                                                                                                                                            |
| Copy                                   | Copy the selected text to the clipboard.                                                                                                                                                                           |
| Paste                                  | Insert the most recently cut or copied text from the clipboard.                                                                                                                                                    |
| Clear                                  | Delete the contents of the selected building block cell.                                                                                                                                                           |
| Find                                   | Open the **Find and Replace** dialog box, where you can search text in the view pane.                                                                                                                              |
| Replace                                | Open the **Find and Replace** dialog box, where you can search and replace text in the view pane.                                                                                                                  |
| Insert Rows from Dimensions            | Open the **Insert Rows from Dimensions** dialog box, where you can select the dimension values to include in the row definition. This command is available from a row definition.                                  |
| Renumber Rows                          | Renumber all numeric row codes. This command is available from a row definition.                                                                                                                                   |
| Row Links                              | Open the **Row Links** dialog box, where you can specify the sources for data links in row definitions and reporting tree definitions. This command is available from a row definition.                            |
| Rounding Adjustment                    | Open the **Rounding Adjustments** dialog box, where you can specify the parameters for rounding. This command is available from a row definition.                                                                  |
| Manage Dimension Sets                  | Open the **Dimension Sets** dialog box, where you can create and modify dimension sets. This command is available from a row definition or reporting tree definition.                                              |
| Insert Row                             | Insert an empty row into the row definition or an empty header row into the column definition. This command is available from a row definition or column definition.                                               |
| Delete Row                             | Delete the selected row from the row definition or the selected header row from the column definition. This command is available from a row definition or column definition.                                       |
| Insert Column                          | Insert an empty column into the column definition. This command is available from a column definition.                                                                                                             |
| Delete Column                          | Delete the selected column from the column definition. This command is available from a column definition.                                                                                                         |
| Insert Reporting Units from Dimensions | Open the **Insert Reporting Units from Dimensions** dialog box, where you can select the dimension values to include in the reporting tree definition. This command is available from a reporting tree definition. |
| Import Dimension Set Hierarchy         | Open the **Dimension Set Hierarchy** dialog box, where you can import a dimension set hierarchy from the financial data. This command is available from a reporting tree definition for a dimension-based system.  |
| Insert Reporting Unit                  | Insert an empty row into the reporting tree definition. This command is available from a reporting tree definition.                                                                                                |
| Delete Reporting Unit                  | Delete the selected reporting unit row from the reporting tree definition. This command is available from a reporting tree definition.                                                                             |

### <a name="view-menu"></a>View menu

The **View** menu is available to all users and includes the following commands.

| Command         | Description                                                            |
|-----------------|------------------------------------------------------------------------|
| Navigation Pane | Show or hide the navigation pane.                                      |
| Toolbars        | Select the toolbars that are visible.                                  |
| Status Bar      | Show or hide the status information in the **Report Designer** window. |
| Welcome Page    | Open the **Welcome** page.                                             |

### <a name="format-menu"></a>Format menu

The **Format** menu is available to users who have the **Designer** or **Administrator** role. This menu includes the following commands.

| Command               | Description                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Styles and Formatting | Open the **Styles and Formatting** dialog box, where you can create and modify the style for text in row definitions and column definitions. This command is available from a row definition or a column definition. |
| Column Width          | Open the **Column Width** dialog box, where you can set the width of the selected column. This command is available from a row definition, a column definition, or a reporting tree definition.                      |
| Hide                  | Hide the selected column. This command is available from a row definition, a column definition, or reporting tree definition.                                                                                        |
| Unhide                | Make the hidden columns between the selected columns visible. This command is available from a row definition, column definition, or reporting tree definition.                                                      |

### <a name="company-menu"></a>Company menu

The **Company** menu is available to users who have the **Designer** or **Administrator** role. This menu includes the following commands.

| Command               | Description                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Companies             | Open the **Companies** dialog box, where you can create and modify companies.                                          |
| Building Block Groups | Open the **Building Block Groups** dialog box, where you can create, modify, import, and export building block groups. |

### <a name="go-menu"></a>Go menu

The **Go** menu is available to all users and includes the following commands. **Note:** These commands have no visible effect unless the navigation pane is visible.

| Commands                   | Description                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Report Definitions         | Show report definitions in the navigation pane.                                    |
| Row Definitions            | Show row definitions in the navigation pane.                                       |
| Column Definitions         | Show column definitions in the navigation pane.                                    |
| Reporting Tree Definitions | Show reporting tree definitions in the navigation pane.                            |
| Security                   | Show security information for users, groups, and companies in the navigation pane. |

### <a name="tools-menu"></a>Tools menu

The **Tools** menu is available to all users, but some commands have limited availability. This menu includes the following commands.

| Command                       | Description                                                                                                                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Protect                       | Apply a password to the current building block. This command is available to users who have the **Designer** or **Administrator** role.                                                                           |
| Report Queue Status           | Open the **Report Queue Status** dialog box, where you can see all recently generated reports and the details for each report.                                                                                    |
| Source System Information     | Show the settings for your Microsoft Dynamics ERP system. This command is available to users who have the **Designer** or **Administrator** role.                                                                 |
| Checked Out Items             | Show the row definitions, column definitions, reporting tree definitions, and report definitions that are currently open. This command is available to users who have the **Designer** or **Administrator** role. |
| Refresh Cached Financial Data | Update the data in the financial dimensions column.                                                                                                                                                               |
| Options                       | Open the **Options** dialog box, where you can modify user preferences for Report Designer.                                                                                                                       |

### <a name="window-menu"></a>Window menu

The **Window** menu is available to all users and includes the following commands.

| Command              | Description                                                                                                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tile Horizontally    | Show all open windows next to each other.                                                                                                                                                     |
| Tile Vertically      | Show all open windows, one on top of the other.                                                                                                                                               |
| Cascade              | Layer all open windows, so that the title bar of each window is visible.                                                                                                                      |
| Freeze Horizontal    | Freeze the selected row so that, as you scroll, that row continues to be visible in the window. This command is available to users who have the **Designer** or **Administrator** role.       |
| Freeze Vertical      | Freeze the selected column so that, as you scroll, that column continues to be visible in the window. This command is available to users who have the **Designer** or **Administrator** role. |
| List of Open Windows | Show a list of windows that are open. Select a window to bring it to the front.                                                                                                               |

### <a name="help-menu"></a>Help menu

The **Help** menu is available to all users and includes the following commands.

| Command | Description                                                  |
|---------|--------------------------------------------------------------|
| Help    | Open the Dynamics AX help wiki page for financial reporting. |
|         |                                                              |

## <a name="report-designer-toolbar-buttons"></a>Report Designer toolbar buttons
The following tables describe the toolbar buttons that you can use when you design reports. Some toolbar buttons are available only in specific circumstances. For example, the buttons for promoting and demoting reporting units are available only when you're modifying a reporting tree definition.

### <a name="standard-toolbar"></a>Standard toolbar

The standard toolbar provides quick access to file and edit commands. This toolbar includes the following buttons.

| Button                                                                                                                                                                                   | Description                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![New button](./media/rowc130389.png)](./media/rowc130389.png)                              | Create a new (empty) report definition, row definition, column definition, or reporting tree definition.                                                                               |
| [![Open button](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Open an existing row definition, column definition, reporting tree definition, or report definition.                                                                                   |
| [![Save button](./media/savec130389.png)](./media/savec130389.png)                           | Save the current row definition, column definition, reporting tree definition, or report definition.                                                                                   |
| [![Copy button](./media/copyc130389.png)](./media/copyc130389.png)                           | Copy the selected text to the clipboard.                                                                                                                                               |
| [![Cut button](./media/cutc130389.png)](./media/cutc130389.png)                              | Delete the selected text, and copy it to the clipboard.                                                                                                                                |
| [![Paste button](./media/pastec130389.png)](./media/pastec130389.png)                        | Insert the text from the clipboard.                                                                                                                                                    |
| [![Undo button](./media/undoc130389.png)](./media/undoc130389.png)                           | Undo the last action.                                                                                                                                                                  |
| [![Redo button](./media/redoc130389.png)](./media/redoc130389.png)                           | Reverse the last undo action.                                                                                                                                                          |
| [![Find button](./media/findc130389.png)](./media/findc130389.png)                           | Open the **Find and Replace** dialog box, where you can search and replace text in the active window.                                                                                  |
| [![Insert row button](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Insert an empty row into the row definition or an empty header row into the column definition. This button is available from a row definition or column definition.                    |
| [![Insert column button](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Insert an empty column into the column definition. This button is available from a column definition.                                                                                  |
| [![Lock button](./media/lockc130389.png)](./media/lockc130389.png)                           | Apply a password to the current building block. This button is available to users who have the **Designer** or **Administrator** role.                                                 |
| [![Row link button](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | Open the **Row Links** dialog box, where you can specify the sources for data links in row definitions and reporting tree definitions. This button is available from a row definition. |
| [![Promote button](./media/promotec130389.png)](./media/promotec130389.png)                  | Promote a unit of the reporting tree definition. When you select a child unit and then click **Promote**, the child unit is moved to the same level as its parent unit.                |
| [![Demote button](./media/demotec130389.png)](./media/demotec130389.png)                     | Demote a unit of the reporting tree definition. When you select a unit and then click **Demote**, the unit becomes a child of the unit that precedes it.                               |
| [![Expand button](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Expand all units of the reporting tree definition at the level of the selected unit.                                                                                                   |
| [![Collapse button](./media/collapsec130389.png)](./media/collapsec130389.png)               | Collapse the reporting tree.                                                                                                                                                           |
| [![Help button](./media/helpc130389.png)](./media/helpc130389.png)                           | Open Help.                                                                                                                                                                             |

### <a name="formatting-toolbar"></a>Formatting toolbar

The formatting toolbar provides easy access to style commands. This toolbar includes the following buttons.

| Button                                                                                                                                                                                                   | Description                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [![Font style button](./media/formattingc130389.png)](./media/formattingc130389.png)                         | Apply the selected font style to the current text.      |
| [![Font button](./media/fonttype.png)](./media/fonttype.png)                                                 | Set the current text to the selected font.              |
| [![Font size button](./media/fontsize.png)](./media/fontsize.png)                                            | Set the current text to selected font size (in points). |
| [![Bold button](./media/boldc130389.png)](./media/boldc130389.png)                                           | Make the current text bold.                             |
| [![Italic button](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | Make the current text italic.                           |
| [![Underline button](./media/underlinec130389.png)](./media/underlinec130389.png)                            | Underline the current text.                             |
| [![Decrease indent button](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | Decrease the indent of the current text.                |
| [![Increase indent button](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | Increase the indent of the current text.                |
| [![Background color button](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | Change the background color of the current cell.        |
| [![Font color button](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | Change the color of the current text.                   |

### <a name="report-designer-toolbar"></a>Report designer toolbar

The report designer toolbar provides quick access to commands for navigating within report designer. This toolbar includes the following buttons.

| Button                                                                                                                                                                                          | Description                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![Report definition button](./media/reportc130389.png)](./media/reportc130389.png)                 | Show the report definition that is listed on the **Window** menu.                                                                                                            |
| [![Row definition button](./media/rowc130389.png)](./media/rowc130389.png)                          | Show the row definition that is assigned to the active report definition.                                                                                                    |
| [![Column definition button](./media/columnc130389.png)](./media/columnc130389.png)                 | Show the column definition that is assigned to the active report definition.                                                                                                 |
| [![Reporting tree definition button](./media/treec130389.png)](./media/treec130389.png)             | Show the reporting tree definition that is assigned to the active report definition.                                                                                         |
| [![Report Viewer button](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | Start the Report Viewer and show the most recent version of the generated report. This button is available from a report definition if you've generated at least one report. |
| [![Generate report button](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Generate a report from the active report definition. This button is available from a report definition.                                                                      |



<a name="see-also"></a>See also
--------

[Financial reporting for Microsoft Dynamics ERP](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics-bi-reporting/management-reporter-for-microsoft-dynamics-erp)

[Generate a financial report](https://docs.microsoft.com/en-us/dynamics365/operations/financials/general-ledger/generate-a-financial-report)




<!--HONumber=Feb17_HO3-->


