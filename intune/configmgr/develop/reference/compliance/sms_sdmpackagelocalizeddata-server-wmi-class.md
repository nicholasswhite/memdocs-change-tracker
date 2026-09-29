---
title: "SMS_SDMPackageLocalizedData Server WMI Class"
description: In Configuration Manager, the SMS_SDMPackageLocalizedData Windows Management Instrumentation class is an SMS Provider server class that represents localized data for a System Definition Model package.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_SDMPackageLocalizedData Server WMI Class

The `SMS_SDMPackageLocalizedData` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents localized data for a System Definition Model (SDM) package.

## Syntax

```
Class SMS_SDMPackageLocalizedData
{
      UInt32 LocaleID;
      String LocalizedData;
};
```

## Methods

The `SMS_SDMPackageLocalizedData` class does not define any methods.

## Properties

`LocaleID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

The ID of the locale associated with the localized information.

`LocalizedData` Data type: `String`

Access type: Read/Write

Qualifiers: None

The localized data.

## Remarks

Class qualifiers for this class include:

- Embedded

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

  This class is embedded by the [SMS_ConfigurationItemBaseClass Server WMI Class](sms_configurationitembaseclass-server-wmi-class.md) through the `SDMPackageLocalizedData` property.

  The application uses this class to add localized string resources to the server database.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Compliance Settings (DCM) Server WMI Classes](compliance-settings-dcm-server-wmi-classes.md) [SMS_Package Server WMI Class](../core/servers/configure/sms_package-server-wmi-class.md)
