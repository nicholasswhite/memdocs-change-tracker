---
title: "SMS_CIDeploymentUnknownAssetDetails Server WMI Class"
description: The SMS_CIDeploymentUnknownAssetDetails WMI class represents the asset-level status of a configuration item deployment for unknown status.
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

# SMS_CIDeploymentUnknownAssetDetails Server WMI Class

The `SMS_CIDeploymentUnknownAssetDetails` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the asset-level status of a configuration item deployment for unknown status.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CIDeploymentUnknownAssetDetails : SMS_BaseClass
{
    UInt32 AssignmentID;
    String AssignmentUniqueID;
    UInt32 Category;
    UInt32 CI_ID;
    String CollectionID;
    String CollectionName;
    UInt32 DeploymentIntent;
    Boolean IsMachineAssignedToUser;
    Boolean IsMachineChangesPersisted;
    Boolean IsVM;
    UInt32 MachineID;
    String MachineName;
    String MachineOS;
    UInt32 PolicyModelID;
    String SoftwareName;
    DateTime StartTime;
    String UserName;
    String VMHostName;
};
```

## Methods

The `SMS_CIDeploymentUnknownAssetDetails` class does not define any methods.

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

Qualifiers: [read]

Category description.

`CI_ID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

Unique ID of the configuration item. This ID is unique only for the site.

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

`IsMachineAssignedToUser` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`IsMachineChangesPersisted` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`IsVM` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`MachineID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`MachineName` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`MachineOS` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Computer operating system.

`PolicyModelID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`SoftwareName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Name of the software.

`StartTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`UserName` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

`VMHostName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

See [SMS_AppDeploymentAssetDetails Server WMI Class](sms_appdeploymentassetdetails-server-wmi-class.md).

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
