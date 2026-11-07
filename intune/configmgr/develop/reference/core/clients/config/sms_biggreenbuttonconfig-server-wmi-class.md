---
description: Learn how to stop clients from connecting to the client notification server with SMS_BigGreenButtonConfig.
title: "SMS_BigGreenButtonConfig Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: iceorbital
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
moniker_range_name: ''
ms.author: acabello
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

# SMS_BigGreenButtonConfig Server WMI Class

The `SMS_BigGreenButtonConfig` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that can stop clients from connecting to the client notification server (a hidden role, co-located with management point).

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_BigGreenButtonConfig : SMS_ClientAgentConfig_BaseClass
{
    UInt32 AgentID;
    Boolean EnableClientNotification;
};
```

## Methods

The `SMS_BigGreenButtonConfig` class doesn't define any methods.

## Properties

`AgentID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, read]

Identifies the client agent component. The BigGreenButton Agent ID is 18.

`EnableClientNotification` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`false` to stop clients from connecting to the client notification server (a hidden role, co-located with management point). No active connections are established between the clients and the client notification server. The default value is `true`.

This setting is part of the client infrastructure and turned on by default. This value would likely only be changed to troubleshoot a significant performance issue.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
