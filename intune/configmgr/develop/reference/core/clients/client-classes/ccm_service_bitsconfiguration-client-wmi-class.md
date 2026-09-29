---
description: Learn how to use CCM_ServiceBITSConfiguration class which supports BITS-related settings used by CCMEXEC for uploading and downloading message payloads.
title: "CCM_Service_BITSConfiguration Client WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
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
