---
title: "SMS_ConfigurationItemSettingReference Server WMI Class"
description: Provides the rule relationship to the settings that are referenced from different configuration items.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_ConfigurationItemSettingReference Server WMI Class

The `SMS_ConfigurationItemSettingReference` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that provides the rule relationship to the settings that are referenced from different configuration items.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ConfigurationItemSettingReference : SMS_BaseClass
{
    UInt32 CI_ID;
    Boolean IsBroken;
    UInt32 Rule_ID;
    UInt32 Setting_ID;
    String SettingName;
};
```

## Methods

The `SMS_ConfigurationItemSettingReference` class does not define any methods.

## Properties

`CI_ID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

[SMS_ConfigurationItemLatestBaseClass Server WMI Class](sms_configurationitemlatestbaseclass-server-wmi-class.md)

`IsBroken` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

[SMS_ConfigurationItem Server WMI Class](sms_configurationitem-server-wmi-class.md)

`Rule_ID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

[SMS_ConfigurationItemRules Server WMI Class](sms_configurationitemrules-server-wmi-class.md)

`Setting_ID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

See [SMS_ConfigurationItemSettings Server WMI Class](sms_configurationitemsettings-server-wmi-class.md).

`SettingName` Data type: `String`

Access type: Read/Write

Qualifiers: none

See [SMS_ConfigurationItemSettings Server WMI Class](sms_configurationitemsettings-server-wmi-class.md).

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
