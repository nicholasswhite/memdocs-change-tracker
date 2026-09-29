---
description: Learn how to represent the fallback relationships for boundary groups in Configuration Manager using SMS_BoundaryGroupRelationships.
title: "SMS_BoundaryGroupRelationships Server WMI Class"
ms.date: "2017-03-13T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_BoundaryGroupRelationships Server WMI Class

The `SMS_BoundaryGroupRelationships` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents fallback relationships for boundary groups.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_BoundaryGroupRelationships : SMS_BaseClass
{
    UInt32 DestinationGroupID;
    String DestinationGroupName;
    UInt32 SourceGroupID;
    String SourceGroupName;
};
```

## Methods

The following table shows the methods in `SMS_BoundaryGroupRelationships`.

| Method | Description |
| --- | --- |
| [FallbackDP Method in Class SMS_BoundaryGroupRelationships](fallbackdp-method-in-class-sms-boundarygrouprelationships.md) | Sets the fallback time for a distribution point (DP). |
| [FallbackMP Method in Class SMS_BoundaryGroupRelationships](fallbackmp-method-in-class-sms-boundarygrouprelationships.md) | Sets the fallback time for a management point (MP). |
| [FallbackSMP Method in Class SMS_BoundaryGroupRelationships](fallbacksmp-method-in-class-sms-boundarygrouprelationships.md) | Sets the fallback time for a state migration point (SMP). |
| [FallbackSUP Method in Class SMS_BoundaryGroupRelationships](fallbacksup-method-in-class-sms-boundarygrouprelationships.md) | Sets the fallback time for a software update point (SUP). |

## Properties

`DestinationGroupID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

ID of the destination boundary group.

`DestinationGroupName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Name of the destination boundary group.

`SourceGroupID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

ID of the source boundary group.

`SourceGroupName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Name of the source boundary group.

## Remarks

Class qualifiers for this class include:

- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_BoundaryGroup Server WMI Class](sms_boundarygroup-server-wmi-class.md)

[Configuration Manager Site Configuration Server WMI Classes](site-configuration-server-wmi-classes.md)
