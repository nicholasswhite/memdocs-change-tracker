---
title: "SMS_DCMDeploymentCompliantStatus Server WMI Class"
description: Learn how to use the SMS_DCMDeploymentCompliantStatus class in Configuration Manager to set the compliant status of a deployment.
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

# SMS_DCMDeploymentCompliantStatus Server WMI Class

The `SMS_DCMDeploymentCompliantStatus` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the compliant status of a deployment.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_DCMDeploymentCompliantStatus : SMS_BaseClass
{
    UInt32 Assets;
    UInt32 AssignmentID;
    String AssignmentUniqueID;
    UInt32 BL_ID;
    String BLName;
    UInt32 BLRevision;
    UInt32 CI_ID;
    String CIName;
    DateTime DeploymentTime;
    UInt32 Revision;
    UInt32 StatusType;
    DateTime SummarizationTime;
    UInt32 SummaryType;
    String TargetCollectionID;
};
```

## Methods

The `SMS_DCMDeploymentCompliantStatus` class does not define any methods.

## Properties

`Assets` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

Number of assets related to the status.

`AssignmentID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

The ID of the configuration item assignment. This ID is unique only for the site.

`AssignmentUniqueID` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_DCMDeploymentCompliantDetailsPerAsset Server WMI Class](sms_dcmdeploymentcompliantdetailsperasset-server-wmi-class.md).

`BL_ID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

See [SMS_DCMDeploymentCompliantDetailsPerAsset Server WMI Class](sms_dcmdeploymentcompliantdetailsperasset-server-wmi-class.md).

`BLName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

See [SMS_DCMDeploymentCompliantDetailsPerAsset Server WMI Class](sms_dcmdeploymentcompliantdetailsperasset-server-wmi-class.md).

`BLRevision` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_DCMDeploymentCompliantDetailsPerAsset Server WMI Class](sms_dcmdeploymentcompliantdetailsperasset-server-wmi-class.md).

`CI_ID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

See [SMS_DCMDeploymentCompliantDetailsPerAsset Server WMI Class](sms_dcmdeploymentcompliantdetailsperasset-server-wmi-class.md).

`CIName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

See [SMS_DCMDeploymentCompliantDetailsPerAsset Server WMI Class](sms_dcmdeploymentcompliantdetailsperasset-server-wmi-class.md).

`DeploymentTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: [not_null, read]

The time of the deployment.

`Revision` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_DCMDeploymentCompliantDetailsPerAsset Server WMI Class](sms_dcmdeploymentcompliantdetailsperasset-server-wmi-class.md).

`StatusType` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

Status of the deployment from the targeted asset. Possible values are:

| Value | Deployment status |
| --- | --- |
| 1 | Success |
| 2 | InProgress |
| 4 | Unknown |

`SummarizationTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: [not_null, read]

Time of the summarization.

`SummaryType` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

Type of the summary.

`TargetCollectionID` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

See [SMS_DCMDeploymentCompliantDetailsPerAsset Server WMI Class](sms_dcmdeploymentcompliantdetailsperasset-server-wmi-class.md).

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
