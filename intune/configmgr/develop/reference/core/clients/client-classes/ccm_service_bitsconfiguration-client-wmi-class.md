---
description: Learn how to use CCM_ServiceBITSConfiguration class which supports BITS-related settings used by CCMEXEC for uploading and downloading message payloads.
title: "CCM_Service_BITSConfiguration Client WMI Class"
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

# CCM_Service_BITSConfiguration Client WMI Class

In Configuration Manager, the `CCM_Service_BITSConfiguration` class is a client Windows Management Instrumentation (WMI) class that supports Background Intelligent Transfer Service (BITS)-related settings used by CCMEXEC for uploading and downloading message payloads. The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class CCM_Service_BITSConfiguration : CCM_Policy
{
      UInt8 DummyKey;
      UInt32 MinimumRetryDelay;
      UInt32 NoProgressTimeout;
      String PolicyID;
      String PolicyInstanceID;
      UInt32 PolicyPrecedence;
      String PolicyRuleID;
      String PolicySource;
      String PolicyVersion;
};
```

## Methods

The `CCM_Service_BITSConfiguration` class does not define any methods.

## Properties

`DummyKey` Data type: `UInt8`

Access type: Read/Write

Qualifiers: None

This value is used as the WMI key for a singleton policy and has no other effect.

`MinimumRetryDelay` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Retry delay to pass to BITS when uploading or downloading message payloads (in minutes). If the value is 0 or `null`, BITS defaults are used.

`NoProgressTimeout` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

No-progress timeout to pass to BITS when uploading or downloading message payloads (in minutes). If the value is `null` or 0, BITS defaults are used.

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

Qualifiers: Key

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

[Client Framework and Data Transfer Client WMI Classes](client-framework-and-data-transfer-client-wmi-classes.md) [CCM_Policy Client WMI Class](ccm_policy-client-wmi-class.md)
