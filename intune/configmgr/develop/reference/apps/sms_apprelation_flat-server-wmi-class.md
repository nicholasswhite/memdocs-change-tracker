---
title: "SMS_AppRelation_Flat Server WMI Class"
description: Details of the SMS_AppRelation_Flat WMI class
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

# SMS_AppRelation_Flat Server WMI Class

The `SMS_AppRelation_Flat` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the flattened application relation. This includes direct and indirect relations.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_AppRelation_Flat : SMS_BaseClass
{
    UInt32 FromApplicationCIID;
    UInt32 FromDeploymentTypeCIID;
    UInt32 Level;
    UInt32 RelationType;
    UInt32 ToApplicationCIID;
    UInt32 ToDeploymentTypeCIID;
};
```

## Methods

The `SMS_AppRelation_Flat` class does not define any methods.

## Properties

`FromApplicationCIID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

From-application configuration item identifier.

`FromDeploymentTypeCIID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

From-deployment type identifier.

`Level` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Level between the from-deployment type and the to-deployment type.

`RelationType` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Type of relationship between configuration items. Possible values are:

| Value | Relationship |
| --- | --- |
| 1 | Bundled |
| 2 | Required |
| 3 | Prohibited |
| 4 | Optional |
| 5 | Derived |
| 6 | Superseded |
| 7 | Self |
| 8 | Reference |
| 9 | AppToDTReference |
| 10 | AppDependence |
| 11 | Intention |
| 12 | Platform |
| 13 | GlobalConditionReference |
| 15 | ApplicationSuperSeded |
| 16 | ApplicationType |
| 17 | ApplicationHost |
| 18 | ApplicationInstaller |
| 19 | SupersedOrDependent |
| 20 | VirtualEnvironmentReference |
| 21 | AppDCMReference |
| 22 | DeploymentTypeToPolicyTemplateReference |
| 23 | CIInheritanceRelation |
| 24 | AppConfigTemplateReference |
| 25 | AppGroupItemReference |

`ToApplicationCIID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

To-application configuration item identifier.

`ToDeploymentTypeCIID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

To-deployment type configuration item identifier.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
