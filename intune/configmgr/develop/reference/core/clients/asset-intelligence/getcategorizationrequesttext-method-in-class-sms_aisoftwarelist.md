---
title: "GetCategorizationRequestText Method in Class SMS_AISoftwareList"
description: The GetCategorizationRequestText retrieves the XML that is sent to System Center Online for categorization.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/aa9d0281-4c35-44bb-8c75-a0920bde2014
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/c7449412-70b0-48ea-831f-3b132eafb97e
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# GetCategorizationRequestText Method in Class SMS_AISoftwareList

The `GetCategorizationRequestText` Windows Management Instrumentation (WMI) class method, in Configuration Manager, retrieves the XML that is sent to System Center Online for categorization.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 GetCategorizationRequestText(
     String SoftwareKey,
     String CategorizationRequestText
);
```

#### Parameters

`SoftwareKey` Data type: `String`

Qualifiers: [in]

The MD5 hash of the software to be categorized. The hash is made up of the software name, publisher, and version.

This property name has changed from `SoftwarePropertiesHash` to `SoftwareKey` in SP1.

`CategorizationRequestText` Data type: `String`

Qualifiers: [out]

XML formatted string which contains the hash, name, version, publisher, evidence type, and system default locale identifier (LCID) of the software.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_AISoftwareList Server WMI Class](sms_aisoftwarelist-server-wmi-class.md)
