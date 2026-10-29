---
title: "SMS_ClientDataSourcesDeviceCounts Server WMI Class"
description: Learn how to use the SMS_ClientDataSourcesDeviceCounts class in Configuration Manager to represent device counts for client data sources.
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

# SMS_ClientDataSourcesDeviceCounts Server WMI Class

The `SMS_ClientDataSourcesContentStats` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents device counts for client data sources.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ClientDataSourcesDeviceCounts : SMS_BaseClass
{
    UInt32 ClientCount;
    UInt32 DPCount;
    UInt32 PeerClientCount;
};

```

## Methods

The `SMS_ClientDataSourcesDeviceCounts` class does not define any methods.

## Properties

`ClientCount` Data type: `UInt32`

Access type: Read

Qualifiers: none

The number of clients.

`DPCount` Data type: `UInt32`

Access type: Read

Qualifiers: none

The number of distribution points.

`PeerClientCount` Data type: `UInt32`

Access type: Read

Qualifiers: none

The number of peer clients.

## Remarks

Class qualifiers for this class include:

- Dynamic
- Read (read-only)
- Singleton
- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
