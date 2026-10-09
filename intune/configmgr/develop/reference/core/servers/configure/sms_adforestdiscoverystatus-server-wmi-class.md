---
description: Learn how to represent the status of Configuration Manager Active Directory Forest Discovery with SMS_ADForestDiscoveryStatus.
title: "SMS_ADForestDiscoveryStatus Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/b1cfdec6-b0c3-4209-818c-736879856e0e
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/37da4cc9-0cfc-42a9-ba5e-805706b01ef8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/2d0723c1-cf38-4c30-ab3d-5df787b33270
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3661fb96-d414-4a4e-b7ad-9370637790dd
---

# SMS_ADForestDiscoveryStatus Server WMI Class

The `SMS_ADForestDiscoveryStatus` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the status of Configuration Manager Active Directory Forest Discovery.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ADForestDiscoveryStatus : SMS_BaseClass
{
    Boolean DiscoveryEnabled;
    UInt32 DiscoveryStatus;
    UInt32 ForestID;
    DateTime LastDiscoveryTime;
    DateTime LastPublishingTime;
    Boolean PublishingEnabled;
    UInt32 PublishingStatus;
    String SiteCode;
    String SiteName;
};
```

## Methods

The `SMS_ADForestDiscoveryStatus` class does not define any methods.

## Properties

`DiscoveryEnabled` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read]

`true` if forest discovery is enabled.

`DiscoveryStatus` Data type: `UInt32`

Access type: Read-only

Qualifiers: [enumeration, read]

Discovery status. Possible values are:

| Value | Discovery status |
| --- | --- |
| 0 | SUCCEEDED |
| 1 | COMPLETED |
| 2 | ACCESS_DENIED |
| 3 | FAILED |
| 4 | STOPPED |

`ForestID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Identifier of the Active Directory forest.

`LastDiscoveryTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

The last time the forest was discovered.

`LastPublishingTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

The last time the forest was published.

`PublishingEnabled` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read]

`true` if Active Directory publishing is enabled.

`PublishingStatus` Data type: `UInt32`

Access type: Read-only

Qualifiers: [enumeration, read]

Publishing status. Possible values are:

| Value | Publishing status |
| --- | --- |
| 0 | UNKNOWN |
| 1 | SUCCEEDED |
| 2 | FAILED |

`SiteCode` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

The site code where the Active Directory forest was discovered.

`SiteName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

The site name where the Active Directory forest was discovered.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
