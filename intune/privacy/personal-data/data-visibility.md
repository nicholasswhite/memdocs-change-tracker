---
title: "View and correct personal data"
description: Learn how to view and correct personal data that's been collected by Intune.
ms.date: "2022-04-08T00:00:00Z"
ms.topic: overview
ms.reviewer: angerobe
ms.collection:
- M365-identity-device-management
- privacy
- sub-data-privacy
author: paolomatarazzo
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/68ec7f3a-2bc6-459f-b959-19beb729907d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/68e4b2d8-b70c-4019-b49a-d1f8881e2aea
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: paoloma
ms.service: microsoft-intune
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/90370425-aca4-4a39-9533-d52e5e002a5d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/67b2ba1a-6f74-4044-a48a-f0f8ad076b8f
---

# View and correct personal data

Based on their access permissions, Intune admins can view some personal data that's been collected by Intune but can't change that data. Only end users can change their device's personal data that has been collected by Intune.

> [!NOTE]
>
> If you're interested in viewing or deleting personal data, see the [Azure Data Subject Requests for the GDPR](https://learn.microsoft.com/en-us/microsoft-365/compliance/gdpr-dsr-azure) article. If you're looking for general info about GDPR, see the [GDPR section of the Service Trust portal](https://servicetrust.microsoft.com/ViewPage/GDPRGetStarted).

## View personal data

Admins can see end user personal information in various Nodes of the Intune UI in the Microsoft Intune admin center. The following articles explain what information admins do and don't have access to:

- [See device details](../../device-management/inventory-and-status/device-details.md) in Intune explains how you can review details about an end user's device.
- [Monitor app information and assignments](../../app-management/monitor-assignments.md) explains how to see details about apps installed on an end user's device.
- The [What information can my company see when I enroll my device? article](../../user-help/enrollment/data-visibility.md) gives end users a list of data that their company can and can't see. It's best to clearly tell your users what kind of data you're collecting and why you're collecting it. This article can be the first step in that transparency.

### Who can view the data?

Microsoft uses strict controls to govern access to customer data, granting the lowest level of access required to complete key tasks and revoking access when it's no longer needed.

You can secure and control access to end user personal data by using role-based administration control (RBAC). For more information, see [RBAC with Microsoft Intune](../../fundamentals/role-based-access-control/overview.md).

You can learn more about Microsoft data practices by reading the Online Services Terms and [Microsoft Online Services Privacy Statement](https://go.microsoft.com/fwlink/p/?linkid=131004&clcid=0x409).

## Correct end user personal data

Admins can't update device or app specific information. If an end user wants to correct any personal data (like the device name), they must do so directly on their device. Such changes are synchronized the next time they connect to Intune.

## Next steps

Find out how to [audit, export, or delete](manage-data-requests.md) personal data in Intune.
