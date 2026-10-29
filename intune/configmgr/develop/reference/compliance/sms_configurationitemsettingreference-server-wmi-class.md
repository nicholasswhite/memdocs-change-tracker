---
title: "SMS_ConfigurationItemSettingReference Server WMI Class"
description: Provides the rule relationship to the settings that are referenced from different configuration items.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
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
