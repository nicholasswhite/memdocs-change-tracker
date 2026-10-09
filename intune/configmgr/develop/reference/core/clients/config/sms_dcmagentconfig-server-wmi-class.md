---
description: Learn how the SMS_DCMAgentConfig Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that specifies how client computers retrieve compliance settings.
title: "SMS_DCMAgentConfig Server WMI Class"
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

# SMS_DCMAgentConfig Server WMI Class

The `SMS_DCMAgentConfig` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that specifies how client computers retrieve compliance settings.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_DCMAgentConfig : SMS_ClientAgentConfig_BaseClass
{
    UInt32 AgentID;
    Boolean Enabled;
    Boolean EnableUserStateManagement;
    UInt32 PerProviderTimeout;
    UInt32 PerScanDefaultPriority;
    UInt32 PerScanTimeout;
    UInt32 PerScanTTL;
};
```

## Methods

The `SMS_DCMAgentConfig` class doesn't define any methods.

## Properties

`AgentID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, read]

Identifies the client agent component. The Settings Management Agent identifier is 1.

`Enabled` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if the agent is enabled.

`EnabledUserStateManagement` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` to enable user state management.

This information applies to System Center 2012 Configuration Manager SP1 or later, and System Center 2012 R2 Configuration Manager or later.

`PerProviderTimeout` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Indicated the timeout value for accessing the provider.

`PerScanDefaultPriority` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Priority of the Settings Management evaluation job. Possible values are:

| Value | Settings scan priority |
| --- | --- |
| priIdle | Idle |
| priNormal | Normal (recommended) |
| priHigh | High |
| priForeground | Foreground |

`PerScanTimeout` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Time after which an in-progress Settings Management evaluation will be canceled.

This property is deprecated.

`PerScanTTL` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Time to live (TTL) for the baseline evaluation result. If a baseline is evaluated and then quickly evaluated again, the second evaluation may be ignored depending TTL value.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
