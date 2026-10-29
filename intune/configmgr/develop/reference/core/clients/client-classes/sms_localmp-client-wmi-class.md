---
title: "SMS_LocalMP Client WMI Class"
description: The SMS_LocalMP class is a client Windows Management Instrumentation class, in Configuration Manager, that represents the local management point.
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

# SMS_LocalMP Client WMI Class

The `SMS_LocalMP` class is a client Windows Management Instrumentation (WMI) class, in Configuration Manager, that represents the local management point.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_LocalMP
{
      String Capabilities;
      UInt32 Index;
      String MasterSiteCode;
      String Name;
      String Protocol;
      String SiteCode;
      UInt32 Version;
};
```

## Methods

The `SMS_LocalMP` class does not define any methods.

## Properties

`Capabilities` Data type: `String`

Access type: Read/Write

Qualifiers: None

Capabilities of the local management point.

`Index` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

For local Management Point rotation.

`MasterSiteCode` Data type: `String`

Access type: Read/Write

Qualifiers: None

The master site code for the local management point.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: None

The name of the local management point.

`Protocol` Data type: `String`

Access type: Read/Write

Qualifiers: None

The network protocol used for the local management point.

`SiteCode` Data type: `String`

Access type: Read/Write

Qualifiers: None

The site code for the site supporting the local management point.

`Version` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

The version of the local management point.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Client Framework and Data Transfer Client WMI Classes](client-framework-and-data-transfer-client-wmi-classes.md)
