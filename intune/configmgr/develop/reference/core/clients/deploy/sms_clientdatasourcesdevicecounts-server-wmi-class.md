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
- https://authoring-docs-microsoft.poolparty.biz/devrel/68cb9039-df60-49b0-8ef8-89ad96497f63
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/725b6df3-93e8-472d-834e-e7e0d2953d35
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
