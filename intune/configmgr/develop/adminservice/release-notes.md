---
title: "Administration service release notes"
description: Information about changes to the administration service with each Configuration Manager release
ms.date: "2020-08-11T00:00:00Z"
ms.subservice: sdk
ms.topic: release-notes
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# Administration service release notes

*Applies to: Configuration Manager (current branch)*

## Changes in version 2006

The WMI route is now case-insensitive. For example, in version 2002, you had to specify `AdminService/wmi/SMS_Site`. Now in version 2006, you can also use `AdminService/wmi/sms_site`

## Changes in version 2002

Starting in version 2002, the administration service automatically uses the site's self-signed certificate. This change helps reduce the friction for easier use of the administration service. The site always generates this certificate. Now the administration service ignores the Enhanced HTTP site setting, as it always uses the site's certificate even if no other site system is using Enhanced HTTP. For more information, see [Enable secure HTTPS communication](set-up.md#enable-secure-https-communication).

New properties for the v1.0 Device class:

- Events on a device: `Device(<ResourceID>)/Events`
- Application on a device: `Device(<ResourceID>)/AvailableApplications?$expand=Application`
- Boundary groups on a device: `Device(<ResourceID>)/BoundaryGroups?$expand=BoundaryGroup`

## Changes in version 1910

- The WMI route now supports static WMI methods. For example:

  ```rest
  Verb: Post
  URI: https://<ProviderFQDN>/AdminService/wmi/SMS_Admin.GetAdminExtendedData
  Body: {"Type":1}
  ```
- The Configuration Manager console now sends console connection health information through the administration service.
- Use OData query options **startswith** and **endswith** on WMI route. For example: `https://<ProviderFQDN>/AdminService/wmi/SMS_Collection?$filter=startswith(Name,'All') eq true`
- Use the Power BI Desktop feature to get data from an **OData feed**. You can then see all WMI entities and their objects in Power BI Desktop to create custom reports.
- The **v1.0** route exposes the **Device** class. For example: `https://<ProviderFQDN>/AdminService/v1.0/Device`

> [!TIP]
>
> For more examples, see [How to use the administration service](usage.md).

### Classes available to the WMI route in version 1910

- SMS_ReplicationGroup
- SMS_BoundaryGroup
- SMS_G_System_DISK
- SMS_G_System_LOGICAL_DISK
- SMS_G_System_OPERATING_SYSTEM
- SMS_G_System_PARTITION
- SMS_G_System_PHYSICAL_DISK
- SMS_G_System_PHYSICAL_MEMORY
- SMS_G_System_X86_PC_MEMORY
- SMS_DistributionDPStatus
- SMS_WinPEOptionalComponentInfo
- SMS_OSDeploymentKitWinPEOptionalComponent
- SMS_WinPEOptionalComponentInBootImage
- SMS_G_System_AdvancedThreatProtectionHealthStatus
- SMS_SearchFolder
- SMS_DPStatusDetails
