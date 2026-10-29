---
title: "SMS_SupportedPlatformsOfflineServicing Server WMI Class"
description: In Configuration Manager, the SMS_SupportedPlatformsOfflineServicing Windows Management Instrumentation class is an SMS Provider server class that used to determine which operating system images can be serviced offline.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_SupportedPlatformsOfflineServicing Server WMI Class

The `SMS_SupportedPlatformsOfflineServicing` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that used to determine which operating system images can be serviced offline.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SupportedPlatformsOfflineServicing : SMS_BaseClass
{
    String Name;
    String OsVersionBuild;
    String ProductType;
};
```

## Methods

The `SMS_SupportedPlatformsOfflineServicing` class does not define any methods.

## Properties

`Name` Data type: `String`

Access type: Read

Qualifiers: [key, not_null]

The name of the operating system that supports offline servicing, such as "Windows 8" or "Windows 8 Server".

`OsVersionBuild` Data type: `String`

Access type: Read

Qualifiers: [key, not_null]

The version and build number of Windows that supports offline servicing, such as 6.0.6001.

`ProductType` Data type: `String`

Access type: Read

Qualifiers: [key, not_null]

Product type. Two string values are used: "WinNT" - to indicate a client operating system type, "ServerNT" - to indicate server operating system type. Possible values are:

| String Value | Operating System Type |
| --- | --- |
| ServerNT | Server |
| WinNT | Client |

## Remarks

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
