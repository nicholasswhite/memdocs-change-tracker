---
description: In Configuration Manager, the CCM_Service_HostedClass class is a client Windows Management Instrumentation class that configures a COM class to be hosted in the CCMEXEC service.
title: "CCM_Service_HostedClass Client WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
---

# CCM_Service_HostedClass Client WMI Class

> [!IMPORTANT]
>
> This class supports the Configuration Manager 2007 infrastructure and is not intended to be used directly from your code.

in Configuration Manager, the `CCM_Service_HostedClass` class is a client Windows Management Instrumentation (WMI) class that configures a COM class to be hosted in the CCMEXEC service.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class CCM_Service_HostedClass : CCM_Policy
{
      String CLSID;
      String Description;
      String PolicyID;
      String PolicyInstanceID;
      UInt32 PolicyPrecedence;
      String PolicyRuleID;
      String PolicySource;
      String PolicyVersion;
};
```

## Methods

The `CCM_Service_HostedClass` class does not define any methods.

## Properties

`CLSID` Data type: `String`

Access type: Read/Write

Qualifiers: [Realkey]

CLSID of the COM class that will be hosted in the service. The class must be registered as an in-process DLL component and be associated with the same application ID as CCMEXEC.

`Description` Data type: `String`

Access type: Read/Write

Qualifiers: None

COM class description.

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

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Client Framework and Data Transfer Client WMI Classes](client-framework-and-data-transfer-client-wmi-classes.md)
