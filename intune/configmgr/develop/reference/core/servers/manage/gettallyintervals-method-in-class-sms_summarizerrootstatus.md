---
description: Learn how to use the GetTallyIntervals method to get an array of tally intervals and the default interval.
title: "GetTallyIntervals Method in Class SMS_SummarizerRootStatus"
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

# GetTallyIntervals Method in Class SMS_SummarizerRootStatus

The `GetTallyIntervals` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets an array of tally intervals and the default interval.

The following syntax is simplified from Managed Object Format (MOF) code and is intended to show the definition of the method.

## Syntax

```
SInt32 GetTallyIntervals(
   String SiteCode,
    String ComponentName,
    String TallyIntervals[],
    String DefaultInterval
);
```

#### Parameters

`SiteCode` Data type: `String`

Qualifiers: [in, SizeLimit("3")]

The site code of the site for which the status is reported.

`ComponentName` Data type: `String`

Qualifiers: [in, SizeLimit("3")]

The name of the component.

`TallyIntervals` Data type: `String` Array

Qualifiers: [out]

The tally intervals.

`DefaultInterval` Data type: `String`

Qualifiers: [out]

The default interval.

## Return Values

An `SInt32` data type.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_SummarizerRootStatus Server WMI Class](sms_summarizerrootstatus-server-wmi-class.md)
