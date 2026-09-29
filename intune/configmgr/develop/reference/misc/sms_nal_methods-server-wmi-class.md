---
title: "SMS_NAL_Methods Server WMI Class"
description: The `SMS_NAL_Methods` Windows Management Instrumentation (WMI) class, in Configuration Manager, defines and manipulates a network abstraction layer (NAL) path.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_NAL_Methods Server WMI Class

The `SMS_NAL_Methods` Windows Management Instrumentation (WMI) class, in Configuration Manager, defines and manipulates a network abstraction layer (NAL) path.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_NAL_Methods : SMS_BaseClass ();

```

## Methods

The following table lists the methods in `SMS_NAL_Methods`.

| Method | Description |
| --- | --- |
| [PackNALPath](packnalpath-method-in-class-sms_nal_methods.md) | Encodes a NAL path from its components. |
| [UnPackNALPath](unpacknalpath-method-in-class-sms_nal_methods.md) | Decodes a NAL path into its components. |

## Properties

The `SMS_NAL_Methods` class does not define any properties.

## Remarks

Class qualifiers for this class include:

- Abstract

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_DistributionPoint Server WMI Class](../core/servers/configure/sms_distributionpoint-server-wmi-class.md) [SMS_SCI_SysResUse Server WMI Class](../core/servers/configure/sms_sci_sysresuse-server-wmi-class.md) [SMS_SystemResourceList Server WMI Class](../core/servers/configure/sms_systemresourcelist-server-wmi-class.md)
