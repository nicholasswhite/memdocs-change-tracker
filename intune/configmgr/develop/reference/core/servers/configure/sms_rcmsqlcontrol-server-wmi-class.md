---
description: The SMS_RcmSqlControl Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager.
title: "SMS_RcmSqlControl Server WMI Class"
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

# SMS_RcmSqlControl Server WMI Class

The `SMS_RcmSqlControl` Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_RcmSqlControl :
{
    SMS_RcmSqlControlProperty Props[];
    String SiteCode;
    String TypeName;
};
```

## Methods

The `SMS_RcmSqlControl` class does not define any methods.

## Properties

`Props` Data type: `SMS_RcmSqlControlProperty` Array

Access type: Read/Write

Qualifiers: none

An array of `SMS_RcmSqlControlProperty` representing properties of the control.

`SiteCode` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

SiteCode.

`TypeName` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

TypeName.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
