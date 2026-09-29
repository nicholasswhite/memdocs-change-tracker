---
title: "DeleteMembershipRule Method in Class SMS_Collection"
description: The DeleteMembershipRule Windows Management Instrumentation class method, in Configuration Manager, deletes a membership rule from the collection.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# DeleteMembershipRule Method in Class SMS_Collection

The `DeleteMembershipRule` Windows Management Instrumentation (WMI) class method, in Configuration Manager, deletes a membership rule from the collection.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 DeleteMembershipRule(
     SMS_CollectionRule collectionRule
);
```

#### Parameters

`collectionRule` Data type: `SMS_CollectionRule`

Qualifiers: [in]

[SMS_CollectionRule Server WMI Class](sms_collectionrule-server-wmi-class.md) object to delete.

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
