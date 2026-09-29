---
title: "SMS_SCFToSite_a Server WMI Class"
description: In Configuration Manager, the SMS_SCFToSite_a WMI class is an SMS Provider server class that uses the SiteCode property to relate SMS_SiteControlFile Server WMI Class objects to SMS_Site Server WMI Class objects.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_SCFToSite_a Server WMI Class

The `SMS_SCFToSite_a` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that uses the `SiteCode` property to relate [SMS_SiteControlFile Server WMI Class](sms_sitecontrolfile-server-wmi-class.md) objects to [SMS_Site Server WMI Class](sms_site-server-wmi-class.md) objects.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SCFToSite_a : SMS_BaseAssociation
{
      ref:SMS_Site Site;
      ref:SMS_SiteControlFile SiteControlFile;
};
```

## Properties

`Site` Data type: `ref:SMS_Site`

Access type: Read/Write

Qualifiers: [key]

Reference to an [SMS_Site Server WMI Class](sms_site-server-wmi-class.md) object path.

`SiteControlFile` Data type: `ref:SMS_SiteControlFile`

Access type: Read/Write

Qualifiers: [key]

Reference to an [SMS_SiteControlFile Server WMI Class](sms_sitecontrolfile-server-wmi-class.md)object path.

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
