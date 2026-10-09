---
description: Learn how to use the CCM_Policy_Assignment2 class to represent a policy assignment in Configuration Manager.
title: "CCM_Policy_Assignment2 Client WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/aa9d0281-4c35-44bb-8c75-a0920bde2014
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/c7449412-70b0-48ea-831f-3b132eafb97e
---

# CCM_Policy_Assignment2 Client WMI Class

In Configuration Manager, the `CCM_Policy_Assignment2` class is a client Windows Management Instrumentation (WMI) class that represents a policy assignment.

This information applies to System Center 2012 Configuration Manager SP1 or later, and System Center 2012 R2 Configuration Manager or later.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class CCM_Policy_Assignment2 : CCM_Policy_Config
{
      String AssignmentCondition;
      String AssignmentCookie;
      String AssignmentID;
      ref:CCM_Policy_Policy AssignmentPolicy;
      String AssignmentSource;
      String AssignmentVersion;
};
```

## Methods

The `CCM_Policy_Assignment2` class does not define any methods.

## Properties

`AssignmentCondition` Data type: `String`

Access type: Read/Write

Qualifiers: None

Assignment condition that determines if the policy should be applied to the assignment. Set this property to NULL if the policy always applies, or to the ID of a particular policy condition, represented by [CCM_Policy_Condition Client WMI Class](ccm_policy_condition-client-wmi-class.md).

`AssignmentCookie` Data type: `String`

Access type: Read/Write

Qualifiers: [Not_Null:ToInstance]

Arbitrary data used by the source authority.

`AssignmentID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Unique ID of the assignment.

`AssignmentPolicy` Data type: `ref:CCM_Policy_Policy`

Access type: Read-only

Qualifiers: [read, Not_Null:ToInstance]

Reference to the policy object to which the assignment applies.

`AssignmentSource` Data type: `String`

Access type: Read/Write

Qualifiers: [key, Not_Null:ToInstance]

Source authority of the assignment.

`AssignmentVersion` Data type: `String`

Access type: Read/Write

Qualifiers: [key, Not_Null:ToInstance ToSubClass]

Version of the assignment.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Policy Agent Client WMI Classes](policy-agent-client-wmi-classes.md) [CCM_Policy_Condition Client WMI Class](ccm_policy_condition-client-wmi-class.md)
