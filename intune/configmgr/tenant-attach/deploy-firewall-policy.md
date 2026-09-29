---
title: "Tenant attach: Create and deploy firewall policies from the admin center"
description: Create and deploy firewall policies from the Microsoft Intune admin center and for Configuration Manager collections.
ms.date: "2021-09-27T00:00:00Z"
ms.topic: install-set-up-deploy
ms.subservice: core-infra
ms.collection: tier3
ms.service: configuration-manager
---

# Tenant attach: Create and deploy firewall policies from the admin center

*Applies to: Configuration Manager (current branch)*

Create Windows Firewall policies in the Microsoft Intune admin center and deploy them to Configuration Manager collections.

## Prerequisites

- Access to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
- An environment that's [tenant attached with uploaded devices](device-sync-actions.md).
- A supported version of Configuration Manager and the corresponding version of the console installed.
  - Upgrade the target devices to the latest version of the Configuration Manager client.
- At least one Configuration Manager collection that's [available for assigning Endpoint security policies](endpoint-security-get-started.md#bkmk_collections)
- Windows Devices that [support this profile for tenant attached devices](endpoint-security-get-started.md#bkmk_supportedprofiles)

## Assign firewall policies to a collection

1. Go to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Endpoint security** &gt; **Firewall** then **Create Policy**.
3. Create a profile with the following settings:

   - **Platform**: Windows 10 and later
     - Only Windows 10 clients can be targeted with firewall policies currently.
   - **Profile**: Microsoft Defender Firewall (ConfigMgr)
4. Select **Create** then give the profile a **Name** and a **Description**.
5. On the **Configuration settings** page, set the firewall settings for the devices. For more information about the available settings, see [Settings for firewall policy for tenant attached devices](https://learn.microsoft.com/en-us/intune/device-configuration/endpoint-security/ref-firewall-settings-tenant-attach?toc=/mem/configmgr/tenant-attach/toc.json&bc=/mem/configmgr/tenant-attach/breadcrumb/toc.json)
6. On the **Assignments** page, select the collections to include for the policy assignment then choose **Next**.
7. Review the settings on the **Review + Create** page and select **Create** when you're done.

## Device Status

You can review the status of endpoint security policies for tenant attached devices. The **Device Status** page can be accessed for all endpoint security policy types for tenant-attached clients. To display the **Device Status** page:

1. Select a policy that's targeted to **ConfigMgr** devices to display the **Overview** page for the policy.
2. Select **Device Status** to display a list of devices targeted by the policy.
3. The **Device Name**, **Compliance State**, and **SMS ID** are displayed for each of the devices on the **Device Status** page.

## Next steps

- [Settings for firewall policy for tenant attached devices](https://learn.microsoft.com/en-us/intune/device-configuration/endpoint-security/ref-firewall-settings-tenant-attach?toc=/mem/configmgr/tenant-attach/toc.json&bc=/mem/configmgr/tenant-attach/breadcrumb/toc.json)
- [Create and deploy endpoint security Antivirus policy to tenant attached devices](deploy-antivirus-policy.md)
- [Create and deploy endpoint security Attack surface reduction policy to tenant attached devices](deploy-asr-policy.md)
- [Create and deploy endpoint security Endpoint Detection and Response policy to tenant attached devices](atp-onboard.md)
