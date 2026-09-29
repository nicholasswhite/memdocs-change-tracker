---
title: FormatSystemMessage Method
description: Learn how the FormatSystemMessage method, in Configuration Manager, formats a system error message by using the error code and optional insertion strings.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# FormatSystemMessage Method

The `FormatSystemMessage` method, in Configuration Manager, formats a system error message by using the error code and optional insertion strings.

## Syntax

```
[VBScript]
SMSFormatMessageCtl.FormatSystemMessage
```

#### Parameters

`MessageID` Data type: `int`

Error message ID.

`InsertionStrings` Data type: `object`

Optional list of insertion strings.

## Return Value

A string.

## Requirements

FormatMessageCtl.dll.

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMSFormatMessageCtl Class](smsformatmessagectl-class.md)
