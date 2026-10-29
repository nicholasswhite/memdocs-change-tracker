---
description: Learn how to represent Automatic Deployment Rule (ADR) deployment settings in Configuration Manager.
title: "SMS_ADRDeploymentSettings Server WMI Class"
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

# SMS_ADRDeploymentSettings Server WMI Class

The `SMS_ADRDeploymentSettings` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents Automatic Deployment Rule (ADR) deployment settings.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ADRDeploymentSettings : SMS_BaseClass
{
    UInt32 ActionID;
    String AssociatedDeploymentID;
    String CollectionID;
    String CollectionName;
    UInt32 DeploymentNumber;
    String DeploymentTemplate;
    Boolean Enabled;
    UInt32 LocaleID;
    String Name;
    Sint32 RuleID;
};

```

## Methods

The `SMS_ADRDeploymentSettings` class does not define any methods.

## Properties

`ActionID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

The action ID.

`AssociatedDeploymentID` Data type: `String`

Access type: Read/Write

Qualifiers: none

Deployment ID for the associated deployment.

`CollectionID` Data type: `String`

Access type: Read/Write

Qualifiers: [not_null]

The collection ID.

`CollectionName` Data type: `String`

Access type: Read/Write

Qualifiers: [not_null]

Name of collection.

`DeploymentNumber` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

The deployment number.

`DeploymentTemplate` Data type: `String`

Access type: Read/Write

Qualifiers: [not_null, lazy]

Deployment template XML for the auto deployment.

`Enabled` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

Specifies whether the deployment is enabled.

`LocaleID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [not_null]

Locale of the auto deployment name and description fields.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: none

Name of the deployment setting.

`RuleID` Data type: `SInt32`

Access type: Read/Write

Qualifiers: [not_null]

ID for the associated automatic deployment rule.

## Remarks

Class qualifiers for this class include:

- Dynamic
- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
