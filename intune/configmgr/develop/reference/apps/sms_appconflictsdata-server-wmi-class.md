---
title: "SMS_AppConflictsData Server WMI Class"
description: The SMS_AppConflictsData Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the conflict of an application deployment configuration.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_AppConflictsData Server WMI Class

The `SMS_AppConflictsData` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the conflict of an application deployment configuration.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_AppConflictsData : SMS_BaseClass
{
    UInt32 AssignmentID;
    String AssignmentUniqueID;
    String CollectionID;
    String ConflictsWith;
    UInt32 DTCI;
    UInt64 DTResultID;
    String MachineName;
    String RequiredBy;
    String UserName;
};
```

## Methods

The `SMS_AppConflictsData` class does not define any methods.

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

`ConflictsWith` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

Name of the conflicting deployment type.

`DTCI` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`DTResultID` Data type: `UInt64`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`MachineName` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`RequiredBy` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

Deployment type that depends on the conflicted deployment.

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
