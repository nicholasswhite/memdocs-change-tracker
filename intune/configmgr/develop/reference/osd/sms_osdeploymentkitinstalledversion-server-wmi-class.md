---
description: Learn how to represent a mapping of server names to an installed Assessment and Deployment Kit (ADK) version using SMS_OSDeploymentKitInstalledVersion class.
title: "SMS_OSDeploymentKitInstalledVersion Server WMI Class"
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

# SMS_OSDeploymentKitInstalledVersion Server WMI Class

The `SMS_OSDeploymentKitInstalledVersion` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a mapping of server names to an installed Assessment and Deployment Kit (ADK) version.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_OSDeploymentKitInstalledVersion : SMS_BaseClass
{
    String DeploymentKitVersion;
    String FQDN;
    UInt32 MachineID;
    String NetBiosName;
};

```

## Methods

The `SMS_OSDeploymentKitInstalledVersion` class does not define any methods.

## Properties

`DeploymentKitVersion` Data type: `String`

Access type: Read/Write

Qualifiers: [not_null]

The version of the deployment kit installed on the computer.

`FQDN` Data type: `String`

Access type: Read/Write

Qualifiers: none

The fully qualified domain name of the computer.

`MachineID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key, not_null]

A unique identifier for the computer.

`NetBiosName` Data type: `String`

Access type: Read/Write

Qualifiers: none

The NetBIOS name of the computer.

## Remarks

Class qualifiers for this class include:

- Dynamic

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
