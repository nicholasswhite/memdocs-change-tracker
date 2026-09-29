---
title: "SMS_WindowsServicingStates Server WMI Class"
description: Describes the SMS_WindowsServicingStates Class.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_WindowsServicingStates Server WMI Class

For internal use only.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_WindowsServicingStates : SMS_BaseClass
{
    String Branch;
    String Build;
    String Name;
    UInt32 State;
};

```

## Methods

The `SMS_WindowsServicingStates` class does not define any methods.

## Properties

`Branch` Data type: `String`

Access type: Read

Qualifiers: [key, not_null]

Reserved for internal use.

`Build` Data type: `String`

Access type: Read

Qualifiers: [key, not_null]

Reserved for internal use.

`Name` Data type: `String`

Access type: Read

Qualifiers: none

Reserved for internal use.

`State` Data type: `UInt32`

Access type: Read

Qualifiers: none

Reserved for internal use.

## Remarks

Class qualifiers for this class include:

- Dynamic
- Read (read-only)
- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
