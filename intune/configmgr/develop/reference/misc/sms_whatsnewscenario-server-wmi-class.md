---
title: "SMS_WhatsNewScenario Server WMI Class"
description: SMS_WhatsNewScenario Server WMI Class is for internal use only.
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

# SMS_WhatsNewScenario Server WMI Class

For internal use only.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_WhatsNewScenario : SMS_BaseClass
{
    String Name;
    Boolean Completed;
};

```

## Methods

The `SMS_WhatsNewScenario` class does not define any methods.

## Properties

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: none

Reserved for internal use.

`Completed` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

Reserved for internal use.

## Remarks

Class qualifiers for this class include:

- Dynamic
- Embedded

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Reference](../configuration-manager-reference.md)
