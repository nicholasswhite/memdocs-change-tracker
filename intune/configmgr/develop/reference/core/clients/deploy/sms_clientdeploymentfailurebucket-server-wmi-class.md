---
description: Learn how to represent a client deployment failure bucket used to get the total number of clients with the same failed state message ID.
title: "SMS_ClientDeploymentFailureBucket Server WMI Class"
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

# SMS_ClientDeploymentFailureBucket Server WMI Class

The `SMS_ClientDeploymentFailureBucket` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a client deployment failure bucket that is used to get the total number of clients with the same failed state message ID.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ClientDeploymentFailureBucket: SMS_BaseClass
{
    UInt32 ClientCount;
    String CollectionID;
    UInt32 LastMessageStateID;
};

```

## Methods

The `SMS_ClientDeploymentFailureBucket` class does not define any methods.

## Properties

`ClientCount` Data type: `UInt32`

Access type: Read

Qualifiers: none

The total number of clients with the specified LastMessageStateID.

`CollectionID` Data type: `String`

Access type: Read

Qualifiers: none

The ID of the collection of which the clients are members.

`LastMessageStateID` Data type: `UInt32`

Access type: Read

Qualifiers: [key]

The ID of the last client deployment state message.

## Remarks

Class qualifiers for this class include:

- Dynamic
- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
