---
title: "SMS_ADSite Server WMI Class"
description: Learn how the SMS_ADSite class is an SMS Provider server class that contains Active Directory sites discovered by Configuration Manager Forest Discovery.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/b1cfdec6-b0c3-4209-818c-736879856e0e
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3661fb96-d414-4a4e-b7ad-9370637790dd
---

# SMS_ADSite Server WMI Class

The `SMS_ADSite` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that contains Active Directory sites discovered by Configuration Manager Forest Discovery.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ADSite : SMS_BaseClass
{
    String ADSiteDescription;
    String ADSiteLocation;
    String ADSiteName;
    UInt32 Flags;
    UInt32 ForestID;
    DateTime LastDiscoveryTime;
    UInt32 SiteID;
};
```

## Methods

The `SMS_ADSite` class does not define any methods.

## Properties

`ADSiteDescription` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Description of the Active Directory site.

`ADSiteLocation` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Location of the Active Directory site.

`ADSiteName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Name of the Active Directory site.

`Flags` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Flags.

`ForestID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

The identifier of Active Directory forest.

`LastDiscoveryTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

The last time this Active Directory site was discovered by Active Directory forest discovery.

`SiteID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

The ID of the site.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
