---
title: "SMS_ADForest Server WMI Class"
description: An SMS Provider server class that contains Active Directory forests discovered by Configuration Manager Forest Discovery.
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

# SMS_ADForest Server WMI Class

The `SMS_ADForest` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that contains Active Directory forests discovered by Configuration Manager Forest Discovery.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ADForest : SMS_BaseClass
{
    String Account;
    String CreatedBy;
    DateTime CreatedOn;
    String Description;
    UInt32 DiscoveredADSites;
    UInt32 DiscoveredDomains;
    UInt32 DiscoveredIPSubnets;
    UInt32 DiscoveredTrusts;
    UInt32 DiscoveryStatus;
    Boolean EnableDiscovery;
    String ForestFQDN;
    UInt32 ForestID;
    String ModifiedBy;
    DateTime ModifiedOn;
    String PublishingPath;
    UInt32 PublishingStatus;
};
```

## Methods

The following table lists the methods in the `SMS_ADForest` class.

| Method | Description |
| --- | --- |
| [DeleteDiscoveryData Method in Class SMS_ADForest](deletediscoverydata-method-in-class-sms_adforest.md) | Removes information gathered by the forest discovery process. |

## Properties

`Account` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Account to discover the Active Directory forest.

`CreatedBy` Data type: `String`

Access type: Read/Write

Qualifiers: none

User that added the Active Directory forest.

`CreatedOn` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

Date the Active Directory forest was added.

`Description` Data type: `String`

Access type: Read/Write

Qualifiers: none

Description of the Active Directory forest.

`DiscoveredADSites` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Count of discovered Active Directory sites.

`DiscoveredDomains` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Count of discovered Active Directory domains.

`DiscoveredIPSubnets` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Count of discovered Active Directory IP subnets.

`DiscoveredTrusts` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Count of discovered Active Directory trusts.

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

`EnableDiscovery` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if Active Directory forest discovery is enabled.

`ForestFQDN` Data type: `String`

Access type: Read/Write

Qualifiers: none

FQDN of the Active Directory forest.

`ForestID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, read]

Identifier of the Active Directory forest.

`ModifiedBy` Data type: `String`

Access type: Read/Write

Qualifiers: none

User that last modified the Active Directory Forest.

`ModifiedOn` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

Date the Active Directory Forest was last modified.

`PublishingPath` Data type: `String`

Access type: Read/Write

Qualifiers: none

Alternate publishing path.

`PublishingStatus` Data type: `UInt32`

Access type: Read-only

Qualifiers: [enumeration, read]

Publishing status. Possible values are:

| Value | Publishing status |
| --- | --- |
| 0 | UNKNOWN |
| 1 | SUCCEEDED |
| 2 | FAILED |

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
