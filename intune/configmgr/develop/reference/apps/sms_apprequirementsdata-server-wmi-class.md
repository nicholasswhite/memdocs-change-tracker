---
title: "SMS_AppRequirementsData Server WMI Class"
description: An SMS Provider server class, in Configuration Manager, that represents the requirements data of an application.
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

# SMS_AppRequirementsData Server WMI Class

The `SMS_AppRequirementsData` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the requirements data of an application.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_AppRequirementsData : SMS_BaseClass
{
    UInt32 AssignmentID;
    String AssignmentUniqueID;
    String CollectionID;
    UInt32 DTCI;
    UInt64 DTResultID;
    UInt32 InstanceGroup;
    String MachineName;
    String RequirementName;
    UInt32 RuleID;
    String SettingName;
    String SettingValue;
    String UniqueRequirementName;
    String UserName;
};
```

## Methods

The `SMS_AppRequirementsData` class does not define any methods.

## Properties

`AssignmentID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`AssignmentUniqueID` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`CollectionID` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`DTCI` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`DTResultID` Data type: `UInt64`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`InstanceGroup` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

Instance group.

`MachineName` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`RequirementName` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

Name of the requirement.

`RuleID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

Identifier of the rule.

`SettingName` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

Name of the setting.

`SettingValue` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

Setting value.

`UniqueRequirementName` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

Unique requirement name.

`UserName` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
