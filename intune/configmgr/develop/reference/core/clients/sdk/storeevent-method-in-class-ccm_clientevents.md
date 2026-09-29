---
title: "StoreEvent Method in Class CCM_ClientEvents"
description: The StoreEvent Windows Management Instrumentation class method generates store events.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# StoreEvent Method in Class CCM_ClientEvents

The `StoreEvent` Windows Management Instrumentation (WMI) class method generates store events.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```

 uint32 StoreEvent
{
     UInt32 DurationMS,
     String ComponentName,
     String EventName,
     String SessionId
 };

```

## Parameters

`DurationMS` Data type: `UInt32`

Qualifiers: [in]

The duration of the event in milliseconds.

`ComponentName` Data type: `String`

Qualifiers: [in]

The name of the component.

`EventName` Data type: `String`

Qualifiers: [in]

The name of the event.

`SessionId` Data type: `String`

Qualifiers: [in]

The ID of the session.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See also

[CCM_ClientEvents Client WMI Class](ccm_clientevents-client-wmi-class.md)
