---
title: "SMS_G_USER_DCMDeploymentCompliantAssetDetails Server WMI Class"
description: The SMS_G_USER_DCMDeploymentCompliantAssetDetails Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents compliant asset details for a deployment.
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

# SMS_G_USER_DCMDeploymentCompliantAssetDetails Server WMI Class

The `SMS_G_USER_DCMDeploymentCompliantAssetDetails` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents compliant asset details for a deployment.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_G_USER_DCMDeploymentCompliantAssetDetails : SMS_G_User
{
    UInt32 AssignmentID;
    UInt32 BL_ID;
    UInt32 CI_ID;
    UInt32 ResourceID;
    UInt32 Rule_ID;
};
```

## Methods

The `SMS_G_USER_DCMDeploymentCompliantAssetDetails` class doesn't define any methods.

## Properties

`AssignmentID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

See [SMS_DCMDeploymentErrorAssetDetails Server WMI Class](../compliance/sms_dcmdeploymenterrorassetdetails-server-wmi-class.md).

`BL_ID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

See [SMS_DCMDeploymentErrorAssetDetails Server WMI Class](../compliance/sms_dcmdeploymenterrorassetdetails-server-wmi-class.md).

`CI_ID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

Configuration item ID.

`ResourceID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

Unique ID, supplied by Configuration Manager, that identifies a client resource. This ID isn't unique across sites.

`Rule_ID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

Rule ID.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
