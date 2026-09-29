---
title: FormatModuleString Method
description: The FormatModuleString method, in Configuration Manager, loads string resources from the resource DLL.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# FormatModuleString Method

The `FormatModuleString` method, in Configuration Manager, loads string resources from the resource DLL.

## Syntax

```
[VBScript]
SMSFormatMessageCtl.FormatModuleString
```

#### Parameters

`ModuleName` Data type: `string`

Name of the module to load. The name can be Srvmsgs.dll, Provmsgs.dll, or Climmsgs.dll.

`MessageID` Data type: `int`

Message ID " combined by using the bitwise OR operation with the severity.

`InsertionStrings` Data type: `object`

Optional list of insertion strings.

## Return Value

A string.

## Remarks

`FormatModuleString` loads a string that is specified by `MessageID` from a string resource in the `ModuleName` module and inserts the supplied strings.

## Requirements

FormatMessageCtl.dll.

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMSFormatMessageCtl Class](smsformatmessagectl-class.md)
