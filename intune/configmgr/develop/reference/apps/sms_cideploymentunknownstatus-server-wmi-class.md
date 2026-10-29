---
description: Learn how to represent the status of a configuration item deployment for unknown status using SMS_CIDeploymentUnknownStatus class.
title: "SMS_CIDeploymentUnknownStatus Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_CIDeploymentUnknownStatus Server WMI Class

The `SMS_CIDeploymentUnknownStatus` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the status of a configuration item deployment for unknown status.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CIDeploymentUnknownStatus : SMS_BaseClass
{
    UInt32 AssignmentID;
    String AssignmentUniqueID;
    UInt32 Category;
    UInt32 CI_ID;
    String CollectionID;
    String CollectionName;
    UInt32 DeploymentIntent;
    UInt32 PolicyModelID;
    String SoftwareName;
    DateTime StartTime;
    UInt32 Total;
};
```

## Methods

The `SMS_CIDeploymentUnknownStatus` class does not define any methods.

## Properties

`AssignmentID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`AssignmentUniqueID` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`Category` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

Status category.

`CI_ID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_ConfigurationItemLatestBaseClass Server WMI Class](../compliance/sms_configurationitemlatestbaseclass-server-wmi-class.md).

`CollectionID` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`CollectionName` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`DeploymentIntent` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`PolicyModelID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

Model ID of the policy.

`SoftwareName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Name of the software.

`StartTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`Total` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Total number of resources in this state.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
