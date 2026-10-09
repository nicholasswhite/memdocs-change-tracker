---
title: "Third-party MDM coexistence with Configuration Manager"
description: Learn about using a third-party MDM service with Configuration Manager
ms.date: "2021-10-05T00:00:00Z"
ms.subservice: co-management
ms.topic: article
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/e0ffb20c-01c6-407b-a9bd-29111652a1dc
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/1433a524-c01f-4b87-beab-670c040dea4f
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/3904bce4-d817-48cf-85fd-b6146fca83b7
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/312f1f05-a431-4193-8a4d-e6245d5966de
---

# Third-party MDM coexistence with Configuration Manager

When you concurrently manage Windows 10 or later devices with both Configuration Manager and Microsoft Intune, this functionality is called [co-management](overview.md). When you manage devices with Configuration Manager and enroll to a third-party MDM service, this functionality is called *coexistence*. Having two management authorities for a single device can be challenging if not properly orchestrated between the two. With co-management, Configuration Manager and Intune balance the [workloads](workloads.md) to make sure there are no conflicts. This interaction doesn't exist with third-party services, so there are limitations with the management capabilities of coexistence.

The Configuration Manager client can coexist with a third-party MDM service on a device running Windows 10 version 1709 or later, and that's joined to Microsoft Entra ID. The device can be either of the following types:

- [Microsoft Entra joined](https://learn.microsoft.com/en-us/azure/active-directory/devices/azureadjoin-plan) only. (This type is sometimes referred to as "cloud domain-joined")
- [Hybrid domain-joined](https://learn.microsoft.com/en-us/azure/active-directory/devices/hybrid-azuread-join-plan), where the device is joined to your on-premises Active Directory and registered with your Microsoft Entra ID.

> [!NOTE]
>
> It doesn't support [personally-owned devices](https://learn.microsoft.com/en-us/windows/client-management/mdm/mdm-enrollment-of-windows-devices#connecting-personally-owned-devices-bring-your-own-device).

When the Configuration Manager client detects that a third-party MDM service is also managing the device, it automatically deactivates certain workloads in Configuration Manager. This behavior allows the MDM service to take over these functions. It also prevents conflicting settings on the client that could adversely impact the device and user experience. The following workloads in Configuration Manager are deactivated in this case:

- Resource access policies for VPN, Wi-Fi, email, and certificate settings
- Application management, including legacy packages
- Software update scanning and installation
- Endpoint protection, the Windows Defender suite of antimalware protection features
- Compliance policy for Conditional Access
- Device configuration
- Office Click-to-Run management

The Configuration Manager client avoids conflict with the third-party management authority by continuing the following read-only operations:

- Hardware and software inventory
- Asset Intelligence
- Software metering
- Power management reporting

For more information on the benefits of co-management with Configuration Manager and Intune, see [Co-management benefits](overview.md#benefits).
