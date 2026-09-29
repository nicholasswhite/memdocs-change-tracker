---
description: Learn how to represent the site install map, which describes the layout of all installed features in Configuration Manager.
title: "SMS_SiteInstallMap Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_SiteInstallMap Server WMI Class

The `SMS_SiteInstallMap` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the site install map, which describes the layout of all installed features.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SiteInstallMap : SMS_BaseClass
{
     String BuildNumber;
     UInt32 FileType;
     String FormatVersion;
     String IMapData;
};
```

## Methods

The following table lists the method in `SMS_SiteInstallMap`.

| Method | Description |
| --- | --- |
| [Refresh Method in Class SMS_SiteInstallMap](refresh-method-in-class-sms_siteinstallmap.md) | Reloads the install map from the database, which repopulates the classes. |

## Properties

`BuildNumber` Data type: `String`

Access type: Read/Write

Qualifiers: [lazy]

Configuration Manager build number.

`FileType` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Reserved. Initialized with a value of 1.

`FormatVersion` Data type: `String`

Access type: Read/Write

Qualifiers: [lazy]

Format version of the install map.

`IMapData` Data type: `String`

Access type: Read-only

Qualifiers: [large, lazy]

Install map data in text format.

## Remarks

Class qualifiers for this class include:

- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

  Use classes derived from [SMS_SiteInstallItemBase Server WMI Class](sms_siteinstallitembase-server-wmi-class.md) to view the install map.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Site Configuration Server WMI Classes](site-configuration-server-wmi-classes.md) [SMS_SiteInstallItemBase Server WMI Class](sms_siteinstallitembase-server-wmi-class.md)
