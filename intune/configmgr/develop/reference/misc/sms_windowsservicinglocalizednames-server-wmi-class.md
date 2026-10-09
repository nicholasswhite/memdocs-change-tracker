---
title: "SMS_WindowsServicingLocalizedNames Server WMI Class"
description: The SMS_WindowsServicingLocalizedNames Server WMI Class is for internal use only.For more information about both the class qualifiers and the property qualifiers, see Configuration Manager Class and Property Qualifiers.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/68cb9039-df60-49b0-8ef8-89ad96497f63
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/725b6df3-93e8-472d-834e-e7e0d2953d35
---

# SMS_WindowsServicingLocalizedNames Server WMI Class

For internal use only.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_WindowsServicingLocalizedNames : SMS_BaseClass
{
    UInt32 LocaleID;
    String Name;
    String Value;
};

```

## Methods

The `SMS_WindowsServicingLocalizedNames` class does not define any methods.

## Properties

`LocaleID` Data type: `UInt32`

Access type: Read

Qualifiers: [key, not_null]

Reserved for internal use.

`Name` Data type: `String`

Access type: Read

Qualifiers: [key, not_null]

Reserved for internal use.

`Value` Data type: `String`

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
