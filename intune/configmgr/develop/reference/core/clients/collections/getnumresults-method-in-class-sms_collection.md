---
description: Learn how to get a count of all members in a collection, not including subcollections using GetNumResults.
title: "GetNumResults Method in Class SMS_Collection"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# GetNumResults Method in Class SMS_Collection

The `GetNumResults` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets a count of all members in a collection, not including subcollections.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 GetNumResults(
     ref:SMS_Collection Collection,
     UInt32 Result
);
```

#### Parameters

`Collection` Data type: `ref:SMS_Collection`

Qualifiers: [in]

Collection ID or object path of the collection. The collection ID is the value of the `CollectionID` property of [SMS_Collection Server WMI Class](sms_collection-server-wmi-class.md).

`Result` Data type: `UInt32`

Qualifiers: [out]

Number of collection members.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Collection Server WMI Class](sms_collection-server-wmi-class.md) [SMS_Site Server WMI Class](../../servers/configure/sms_site-server-wmi-class.md)
