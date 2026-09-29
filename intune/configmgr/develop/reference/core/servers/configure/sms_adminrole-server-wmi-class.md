---
title: "SMS_AdminRole Server WMI Class"
description: The SMS_AdminRole Windows Management Instrumentation class is an SMS Provider server class, in Configuration Manager, that represents the association between the admin account and the security role.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_AdminRole Server WMI Class

The `SMS_AdminRole` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the association between the admin account and the security role.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_AdminRole : SMS_BaseClass
{
    UInt32 AdminID;
    String RoleID;
};
```

## Methods

The `SMS_AdminRole` class does not define any methods.

## Properties

`AdminID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

ID of the admin account.

`RoleID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

ID of the security role.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
