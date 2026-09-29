---
title: "How to configure hardware inventory in Configuration Manager"
description: Set up hardware inventory for all clients or for a collection in Configuration Manager.
ms.date: "2017-02-22T00:00:00Z"
ms.subservice: core-infra
ms.topic: how-to
ms.collection: tier3
ms.service: configuration-manager
---

# How to configure hardware inventory in Configuration Manager

*Applies to: Configuration Manager (current branch)*

This procedure configures the default client settings for hardware inventory and will apply to all the clients in your hierarchy. If you want these settings to apply to only some clients, create a custom device client setting and assign it to a collection that contains the devices that you want to use hardware inventory. See [How to configure client settings](../../deploy/configure-client-settings.md).

> [!NOTE]
>
> If a client device receives hardware inventory settings from multiple sets of client settings, then the hardware inventory classes from each set of settings will be merged when the client reports hardware inventory. Additionally, not checking a class in a custom client setting with a higher priority doesn't disable the client from inventorying that class.

To disable a specific hardware inventory class on a majority of systems except a few, the class needs to be unchecked in the default client settings. Then create a custom client setting to enable the class, and deploy it to the target systems.

### To configure hardware inventory

1. In the Configuration Manager console, choose **Administration** &gt; **Client Settings** &gt; **Default Client Settings**.
2. On the **Home** tab, in the **Properties** group, choose **Properties**.
3. In the **Default Settings** dialog box, choose **Hardware Inventory**.
4. In the **Device Settings** list, configure the following:

   - **Enable hardware inventory on clients** - Select **Yes**.
   - **Hardware inventory schedule** - Click **Schedule** to specify the interval at which clients collect hardware inventory.
5. Configure other [hardware inventory client settings](../../deploy/about-client-settings.md#hardware-inventory) that you require.

Client devices will be configured with these settings when they next download client policy. To initiate policy retrieval for a single client, see [How to manage clients](../manage-clients.md).
