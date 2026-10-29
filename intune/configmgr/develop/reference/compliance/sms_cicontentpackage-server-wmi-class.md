---
title: "SMS_CIContentPackage Server WMI Class"
description: The SMS_CIContentPackage WMI class represents the relationship between configuration item and associated content to SMS Package where the binary content is packaged and distributed.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_CIContentPackage Server WMI Class

The `SMS_CIContentPackage` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, represents the relationship between configuration item and associated content to `SMS Package` where the binary content is packaged and distributed.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CIContentPackage : SMS_BaseClass
{
    UInt32 CI_ID;
    UInt32 CI_SecuredTypeID;
    String CI_UniqueID;
    String ModelName;
    String PackageID;
};
```

## Methods

The `SMS_CIContentPackage` class does not define any methods.

## Properties

`CI_ID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

[SMS_ConfigurationItemLatestBaseClass Server WMI Class](sms_configurationitemlatestbaseclass-server-wmi-class.md)

`CI_SecuredTypeID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

CI_SecuredTypeID is the associated RBAC security object type, depending on which object content (Application, Software Update and so on) is part of this package.

`CI_UniqueID` Data type: `String`

Access type: Read/Write

Qualifiers: none

[SMS_ConfigurationItemLatestBaseClass Server WMI Class](sms_configurationitemlatestbaseclass-server-wmi-class.md)

`ModelName` Data type: `String`

Access type: Read/Write

Qualifiers: none

[SMS_ConfigurationItemLatestBaseClass Server WMI Class](sms_configurationitemlatestbaseclass-server-wmi-class.md)

`PackageID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

[SMS_PackageBaseclass Server WMI Class](../core/servers/configure/sms_packagebaseclass-server-wmi-class.md)

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
