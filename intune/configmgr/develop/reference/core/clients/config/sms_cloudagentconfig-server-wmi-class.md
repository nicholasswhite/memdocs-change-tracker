---
title: "SMS_CloudAgentConfig Server WMI Class"
description: The SMS_CloudAgentConfig WMI class is an SMS Provider server class in Configuration Manager.
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

# SMS_CloudAgentConfig Server WMI Class

The `SMS_CloudAgentConfig` Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CloudAgentConfig : SMS_ClientAgentConfig_BaseClass
{
    UInt32 AgentID;
    Boolean AllowCloudDP;
};
```

## Methods

The `SMS_CloudAgentConfig` class does not define any methods.

## Properties

`AgentID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, read]

AgentID

`AllowCloudDP` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

AllowCloudDP

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
