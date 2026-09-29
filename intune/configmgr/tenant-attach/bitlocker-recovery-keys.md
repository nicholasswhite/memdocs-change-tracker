---
title: "Tenant attach: BitLocker recovery keys"
description: View BitLocker recovery keys for tenant-attached devices from the Microsoft Intune admin center.
ms.date: "2022-01-25T00:00:00Z"
ms.topic: how-to
ms.subservice: core-infra
ms.collection: tier3
ms.service: configuration-manager
---

# Tenant attach: BitLocker recovery keys

*Applies to: Configuration Manager (current branch)*

You can get BitLocker recovery keys for a tenant-attached device from the Microsoft Intune admin center. For example, a help desk technician who doesn't have access to Configuration Manager could use the web-based admin center to help an end user get a recovery key for their device.

## Prerequisites

- Configuration Manager site version 2107 or later

  To support devices that are joined to Microsoft Entra ID, install the [update rollup](../hotfix/2107/11121541.md) for Configuration Manager version 2107.
- Apply a Configuration Manager [BitLocker management](../protect/deploy-use/bitlocker/deploy-management-agent.md) policy to the device.

## Permissions

The administrative user needs the following permissions:

- On the **Collection** object that's scoped to a collection that includes the device:

  - **Read**
  - **Read BitLocker Recovery Key**
- An [Intune role](../../fundamentals/role-based-access-control/overview.md) assigned to the user

## View recovery keys

1. In a browser, go to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. In the admin center, select **Devices** and then **All Devices**.
3. Select a device that's synced from Configuration Manager via [tenant attach](device-sync-actions.md).
4. Select **Recovery keys** in the device menu. You'll see the list of encrypted drives on the device.
5. To display a recovery key for a drive, select **Show recovery key**. This action reveals the recovery key, which causes the device to rotate its recovery key. Select **Yes** to continue and view the key.
6. A pane to the right displays the device information, including the BitLocker recovery key. Select the copy icon to copy the key to the clipboard. This action makes it easier to share with a user.

![Recovery Keys pane in the Microsoft Intune admin center.](media/6979225-bitlocker-recovery-key.png)

## Next steps

[Deploy BitLocker management](../protect/deploy-use/bitlocker/deploy-management-agent.md)
