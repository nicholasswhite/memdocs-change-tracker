---
title: "SMS_ContextMethods Server WMI Class"
description: The SMS_ContextMethods Windows Management Instrumentation (WMI) class is an abstract class in Configuration Manager that contains methods for caching WMI context qualifiers with the SMS Provider.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_ContextMethods Server WMI Class

The `SMS_ContextMethods` Windows Management Instrumentation (WMI) class is an abstract class in Configuration Manager that contains methods for caching WMI context qualifiers with the SMS Provider.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ContextMethods ();
```

## Methods

The following table lists the methods in `SMS_ContextMethods`.

| Term | Description |
| --- | --- |
| [ClearContextHandle Method in Class SMS_ContextMethods](clearcontexthandle-method-in-class-sms_contextmethods.md) | Releases cached context data. |
| [GetContextHandle Method in Class SMS_ContextMethods](getcontexthandle-method-in-class-sms_contextmethods.md) | Caches multiple context qualifiers within the SMS Provider. This allows applications to use a much smaller context object when making API calls to WMI. |

## Properties

The `SMS_ContextMethods` class doesn't define any properties.

## Remarks

Class qualifiers for this class include:

- Abstract

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Context Qualifiers](../../core/understand/context-qualifiers.md)
