---
title: "SMS_DeviceMethods Server WMI Class"
description: The SMS_DeviceMethods WMI class is an SMS Provider server class that provides access to actions that you can take on mobile devices and Microsoft Exchange ActiveSync devices.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_DeviceMethods Server WMI Class

The `SMS_DeviceMethods` Windows Management Instrumentation (WMI) class is an SMS Provider server class that provides access to actions that you can take on mobile devices and Microsoft Exchange ActiveSync devices.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_DeviceMethods : SMS_Baseclass ();
```

## Methods

The following table shows the methods in `SMS_DeviceMethods`.

| Method | Description |
| --- | --- |
| [AllowAccess Method in Class SMS_DeviceMethods](allowaccess-method-in-class-sms_devicemethods.md) | Lets the Exchange ActiveSync device connect to Exchange. |
| [BlockAccess Method in Class SMS_DeviceMethods](blockaccess-method-in-class-sms_devicemethods.md) | Blocks the Exchange ActiveSync device from accessing to Exchange. |
| [NEW SP1: CancelRetire Method in Class SMS_DeviceMethods](cancelretire-method-in-class-sms_devicemethods.md) | Cancels the retirement of this device from Configuration Manager. |
| [CancelWipe Method in Class SMS_DeviceMethods](cancelwipe-method-in-class-sms_devicemethods.md) | Cancels a pending wipe request on mobile devices or Exchange ActiveSync devices. |
| [NEW SP1: RequestRetire Method in Class SMS_DeviceMethods](requestretire-method-in-class-sms_devicemethods.md) | Retires this device from Configuration Manager. |
| [RequestWipe Method in Class SMS_DeviceMethods](requestwipe-method-in-class-sms_devicemethods.md) | Removes Microsoft Exchange and Configuration Manager software from the mobile device or Exchange ActiveSync device. |

## Properties

The `SMS_DeviceMethods` class does not define any properties.

## Remarks

Class qualifiers for this class include:

- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

  Mobile device setting packages use programs, distribution points, and advertisements to collections to distribute their content.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[Device Management Server WMI Classes](device-management-server-wmi-classes.md) [SMS_PackageBaseclass Server WMI Class](../core/servers/configure/sms_packagebaseclass-server-wmi-class.md)
