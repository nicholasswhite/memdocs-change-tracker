---
description: The SMS_SecondarySiteStatus WMI class is an SMS Provider server class, in Configuration Manager, that represents secondary site installation or uninstallation status.
title: "SMS_SecondarySiteStatus Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
---

# SMS_SecondarySiteStatus Server WMI Class

The `SMS_SecondarySiteStatus` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents secondary site installation or uninstallation status.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SecondarySiteStatus : SMS_BaseClass
{
    String Description;
    DateTime MessageTime;
    String SiteCode;
    UInt32 SiteInstallID;
    String Status;
    UInt32 StatusID;
};
```

## Methods

The `SMS_SecondarySiteStatus` class does not define any methods.

## Properties

`Description` Data type: `String`

Access type: Read

Qualifiers: none

Description of the status for secondary installation or uninstallation status.

`MessageTime` Data type: `DateTime`

Access type: Read

Qualifiers: [key]

Time of the message reported for the secondary site installation or uninstallation.

`SiteCode` Data type: `String`

Access type: Read

Qualifiers: [key]

Site code of the secondary site.

`SiteInstallID` Data type: `UInt32`

Access type: Read

Qualifiers: [key]

Site installation or uninstallation identifier.

`Status` Data type: `String`

Access type: Read

Qualifiers: none

Secondary site installation or uninstallation status.

`StatusID` Data type: `UInt32`

Access type: Read

Qualifiers: [key]

Identifier for the status.

## Remarks

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
