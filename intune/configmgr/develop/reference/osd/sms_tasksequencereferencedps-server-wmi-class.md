---
title: "SMS_TaskSequenceReferenceDps Server WMI Class"
description: Learn about the simplified syntax, methods, properties, and requirements of the SMS_TaskSequenceReferenceDps server class.
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

# SMS_TaskSequenceReferenceDps Server WMI Class

The `SMS_TaskSequenceReferenceDps` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the package that is available for the task sequence at a specified distribution point.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequenceReferenceDps
{
      String Hash;
      String PackageID;
      String ServerNALPath;
      String SiteCode;
      UInt32 SourceVersion;
      String TaskSequenceID;
};
```

## Methods

The `SMS_TaskSequenceReferenceDps` class does not define any methods.

## Properties

`Hash` Data type: `String`

Access type: Read/Write

Qualifiers: None

A hash of package content.

`PackageID` Data type: `String`

Access type: Read/Write

Qualifiers: None

The ID of the package associated with the task sequence.

`ServerNALPath` Data type: `String`

Access type: Read/Write

Qualifiers: None

The server network abstraction layer (NAL) path to the package at a particular distribution point.

`SiteCode` Data type: `String`

Access type: Read/Write

Qualifiers: None

The site code for the distribution point.

`SourceVersion` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

The version of the package source.

`TaskSequenceID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

The ID for the task sequence.

## Remarks

Class qualifiers for this class include:

- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
