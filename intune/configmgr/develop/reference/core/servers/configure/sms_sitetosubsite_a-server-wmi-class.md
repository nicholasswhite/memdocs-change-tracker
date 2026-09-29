---
title: "SMS_SiteToSubSite_a Server WMI Class"
description: In Configuration Manager, the SMS_SiteToSubSite_a WMI class is an SMS Provider server class that defines the hierarchy of sites by relating an SMS_Site Server WMI Class object with its subsites.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_SiteToSubSite_a Server WMI Class

The `SMS_SiteToSubSite_a` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that defines the hierarchy of sites by relating an [SMS_Site Server WMI Class](sms_site-server-wmi-class.md) object with its subsites.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SiteToSubSite_a : SMS_BaseAssociation
{
      ref:SMS_Site childSite;
      ref:SMS_Site parentSite;
};
```

## Methods

The `SMS_SiteToSubSite_a` class does not define any methods.

## Properties

`childSite` Data type: `ref:SMS_Site`

Access type: Read/Write

Qualifiers: [key]

Reference to an [SMS_Site Server WMI Class](sms_site-server-wmi-class.md) object path for the child site.

`parentSite` Data type: `ref:SMS_Site`

Access type: Read/Write

Qualifiers: [key]

Reference to an `SMS_Site` object path for the parent site.

## Remarks

Class qualifiers for this class include:

- Association: ToInstance
- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Site Configuration Server WMI Classes](site-configuration-server-wmi-classes.md)
