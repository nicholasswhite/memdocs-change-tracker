---
title: "SMS_CIContentPackage Server WMI Class"
description: The SMS_CIContentPackage WMI class represents the relationship between configuration item and associated content to SMS Package where the binary content is packaged and distributed.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
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
