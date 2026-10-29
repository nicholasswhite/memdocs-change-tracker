---
title: "CCM_Service_SystemTaskConfiguration Client WMI Class"
description: In Configuration Manager, the CCM_Service_SystemTaskConfiguration class is a client WMI class that supports system task configuration for the CCMEXEC service.
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

# CCM_Service_SystemTaskConfiguration Client WMI Class

> [!IMPORTANT]
>
> This class supports the Configuration Manager 2007 infrastructure and is not intended to be used directly from your code.

in Configuration Manager, the `CCM_Service_SystemTaskConfiguration` class is a client Windows Management Instrumentation (WMI) class that supports system task configuration for the CCMEXEC service.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class CCM_Service_SystemTaskConfiguration : CCM_Policy
{
      String CoClass;
      String DisplayName;
      String Event;
      String Name;
      UInt32 Order;
      String PolicyID;
      String PolicyInstanceID;
      UInt32 PolicyPrecedence;
      String PolicyRuleID;
      String PolicySource;
      String PolicyVersion;
      String ThreadType;
};
```

## Methods

The `CCM_Service_SystemTaskConfiguration` class does not define any methods.

## Properties

`CoClass` Data type: `String`

Access type: Read/Write

Qualifiers: None

Class ID or program ID of the COM class that implements the system task.

`DisplayName` Data type: `String`

Access type: Read/Write

Qualifiers: None

Display name of the system task.

`Event` Data type: `String`

Access type: Read/Write

Qualifiers: None

Event on which the system task should be invoked.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [Realkey]

Name of the system task, which must be unique on the computer.

`Order` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Order value of the task. Tasks with lower order values run before tasks with higher values. Tasks with the same order value run simultaneously (no ordering between them is guaranteed).This value defaults to 0 if a value is not specified.

`PolicyID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

See [CCM_Policy Client WMI Class](ccm_policy-client-wmi-class.md).

`PolicyInstanceID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

See [CCM_Policy Client WMI Class](ccm_policy-client-wmi-class.md).

`PolicyPrecedence` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

See [CCM_Policy Client WMI Class](ccm_policy-client-wmi-class.md).

`PolicyRuleID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

See [CCM_Policy Client WMI Class](ccm_policy-client-wmi-class.md).

`PolicySource` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

See [CCM_Policy Client WMI Class](ccm_policy-client-wmi-class.md).

`PolicyVersion` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

See [CCM_Policy Client WMI Class](ccm_policy-client-wmi-class.md).

`ThreadType` Data type: `String`

Access type: Read/Write

Qualifiers: None

Thread type on which the endpoint should be invoked.

## Remarks

There is an instance of this class for each system task on the computer.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Client Framework and Data Transfer Client WMI Classes](client-framework-and-data-transfer-client-wmi-classes.md)
