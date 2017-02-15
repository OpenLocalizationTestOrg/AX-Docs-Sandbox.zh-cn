---
title: POS offline functionality | Microsoft Docs
description: This article provides information about offline mode for Retail Modern POS, in which POS devices automatically switch from the channel database to the offline database if the retail server is unavailable. This article also includes general setup information for offline mode and explains the data synchronization that occurs between the offline database and the channel database.
author: josaw1
manager: AnnBe
ms.date: 2015-12-13 04:13:51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: annbe
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 27041
ms.assetid: 3ff2b755-5207-4031-9731-8fcd5f88e406
ms.region: Global
ms.industry: Retail
ms.author: josaw
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 477196312e73e4a9fbc1031fb8072b1e42a599ff


---

# <a name="pos-offline-functionality"></a>POS offline functionality

This article provides information about offline mode for Retail Modern POS, in which POS devices automatically switch from the channel database to the offline database if the retail server is unavailable. This article also includes general setup information for offline mode and explains the data synchronization that occurs between the offline database and the channel database.

<a name="overview"></a>Overview
--------

In Retail Modern POS, a point of sale (POS) device goes into offline mode whenever the retail server is unavailable. Therefore, if the connection with the retail server is lost, Retail Modern POS automatically switches to the offline database. During a sales transaction, if a data request doesn't succeed within the time-out interval that is configured in the offline profile, Retail Modern POS automatically switches to the offline database and continues the sales transaction. While POS device is in offline mode, Retail Modern POS tries to reconnect to the retail server after the reconnection attempt interval that is configured in the offline profile. This reconnection attempt occurs only at the beginning of a transaction.

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>Determining the connection mode of Retail Modern POS

The status header in Retail Modern POS indicates the current connection status, and the **Connection status** window shows the status of the last attempt to sync with the offline database. [![Connection status](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>Creating a button to manually switch between online and offline modes

You can add a button to Retail Modern POS to manually switch between online and offline modes. Create a button for POS operation **917 – Database connection status**. The name of this button is **Disconnect** when Retail Modern POS is connected to the retail server and **Connect** when it is disconnected. You can use this button to view the connection, and to disconnect from the retail server or connect to it. [![Disconnect button in Retail Modern POS](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>Setup
To enable offline support for a POS device (register), set the **Support offline** option to **Yes** on the **Register** page. A new channel database entity is created and added to the store's channel data group. Then run all the required distribution schedules to generate the data packages for the offline database. Next, install the offline version of Retail Modern POS. The installation process creates the offline database. Additionally, install Microsoft SQL Server 2014 Express if it is required. Offline data synchronization starts after the first sign-in to Retail Modern POS.

## <a name="data-synchronization"></a>Data synchronization
The Retail scheduler is used to send master data to the offline database. By default, when a distribution schedule is run, data changes are sent to both the channel database and the offline database. Retail Modern POS includes the async sync library, which downloads any available data packages and inserts them into the offline database. If any transactions are created offline, Retail Modern POS uploads them to the retail server, so that they can be inserted into the channel database. Offline data synchronization can occur only if Retail Modern POS is running. [![Offline synchronization](./media/offline-sync-1024x521.png)](./media/offline-sync.png)




<!--HONumber=Feb17_HO3-->


