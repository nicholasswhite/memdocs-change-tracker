---
title: "SMS_Resource Server WMI Class"
description: In Configuration Manager, the SMS_Resource WMI class is an SMS Provider server class that serves as an abstract base class for all discovery resource classes.
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

# SMS_Resource Server WMI Class

The `SMS_Resource` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that serves as an abstract base class for all discovery resource classes, for example, [SMS_R_IPNetwork Server WMI Class](sms_r_ipnetwork-server-wmi-class.md).

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_Resource : SMS_BaseClass
{
     UInt32 ResourceID;
};
```

## Methods

The `SMS_Resource` class doesn't define any methods.

## Properties

`ResourceID` Data type: **UInt32**

Access type: Read/Write

Qualifiers: [key]

Configuration Manager-supplied ID that uniquely identifies a Configuration Manager client resource. This ID isn't unique across sites. The default value is ''".

## Remarks

Class qualifiers for this class include:

- Abstract
- Read:ToSubClass

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_ResourceMap Server WMI Class](sms_resourcemap-server-wmi-class.md)
