---
description: Learn how to use the SMS_MDMDeviceCategory class to represent an On-premises Mobile Device Management (MDM) device category.
title: "SMS_MDMDeviceCategory Server WMI Class"
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

# SMS_MDMDeviceCategory Server WMI Class

The `SMS_MDMDeviceCategory` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents an On-premises Mobile Device Management (MDM) device category.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_MDMDeviceCategory : SMS_BaseClass
{
    String CategoryID;
    String Name;
};

```

## Methods

The `SMS_MDMDeviceCategory` class does not define any methods.

## Properties

`CategoryID` Data type: `String`

Access type: Read-only

Qualifiers: [key]

Category ID.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [not_null]

Category name.

## Remarks

Class qualifiers for this class include:

- Dynamic
- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
