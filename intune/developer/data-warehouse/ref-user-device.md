---
title: "Reference for User Device Association entity"
description: The UserDeviceAssociation entity contains user device associations in your organization.
ms.date: "2024-10-30T00:00:00Z"
ms.topic: reference
author: nicholasswhite
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: nwhite
ms.collection: M365-identity-device-management
ms.reviewer: jamiesil
ms.service: microsoft-intune
ms.subservice: developer
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
---

# Reference for User Device Association entity

The **userDeviceAssociation** entity contains user device associations in your organization.

## userDeviceAssociations

| Name | Description | Example |
| --- | --- | --- |
| userKey | Unique identifier of the user in the data warehouse. (Surrogate key). | 123 |
| deviceKey | Unique identifier of the device in the data warehouse. | 123 |
| createdDateTimeUTC | Date and time when the user device association was created. Uses UTC format. | 11/23/2016 12:00:00 AM |
| isDeleted | Indicates that the user unenrolled that device, and that the association is not current anymore. | True/False |
| endedDateTimeUTC | Date and time in UTC when IsDeleted changed to **True**. | 06/23/2017 12:00:00 AM |

## Next steps

- Learn more about the [Intune Data Warehouse](create-reports.md).
