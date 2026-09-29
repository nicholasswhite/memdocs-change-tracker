---
description: Learn how to use the SMS_MDMDeviceCategory class to represent an On-premises Mobile Device Management (MDM) device category.
title: "SMS_MDMDeviceCategory Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
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
