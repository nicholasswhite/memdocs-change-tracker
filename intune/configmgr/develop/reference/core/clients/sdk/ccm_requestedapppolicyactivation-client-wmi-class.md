---
title: "CCM_RequestedAppPolicyActivation Client WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
description: Learn how the CCM_RequestedAppPolicy Activation class represents a requested application policy activation.
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

# CCM_RequestedAppPolicyActivation Client WMI Class

The `CCM_RequestedAppPolicyActivation` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a requested application policy activation.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class CCM_RequestedAppPolicyActivation :
{
    UInt32 ActivationAction;
    String AppId;
    DateTime DateRequested;
    Boolean IsComplete;
    String PolicyId;
    String Revision;
    String UserSID;
};
```

## Methods

The following table lists the methods in the `CCM_RequestedAppPolicyActivation` class.

- [QueueAppPolicyActivationAction Method in Class CCM_RequestedAppPolicyActivation](queueapppolicyactivationaction-method-in-class-ccm_requestedapppolicyactivation.md)

## Properties

`ActivationAction` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [values]

Activation action. Possible values are:

| Value | Activation action |
| --- | --- |
| 0 | default |
| 1 | By-pass Activation |

`AppId` Data type: `String`

Access type: Read/Write

Qualifiers: none

Application identifier.

`DateRequested` Data type: `DateTime`

Access type: Read/Write

Qualifiers: none

Date requested.

`IsComplete` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if activation is complete.

`PolicyId` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Policy identifier.

`Revision` Data type: `String`

Access type: Read/Write

Qualifiers: none

Application revision.

`UserSID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

User security identifier (SID).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
