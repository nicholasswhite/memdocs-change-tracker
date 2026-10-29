---
title: SMSFormatMessageCtl Class
description: The SMSFormatMessageCtl class supports message formatting for the Configuration Manager status system.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMSFormatMessageCtl Class

The `SMSFormatMessageCtl` class supports message formatting for the Configuration Manager status system.

## Methods

The following table lists the methods in `SMSFormatMessageCtl`.

| Method | Description |
| --- | --- |
| [FormatModuleMessage Method](formatmodulemessage-method.md) | Resolves Configuration Manager status messages in Srvmsgs.dll, Provmsgs.dll, and Climmsgs.dll. |
| [FormatModuleString Method](formatmodulestring-method.md) | Loads string resources out of the resource DLL. |
| [FormatSystemMessage Method](formatsystemmessage-method.md) | Formats a system error message by using the error code and optional insertion strings. |

## Requirements

FormatMessageCtl.dll.

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
