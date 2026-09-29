---
title: "DeleteAssociation Method in Class SMS_StateMigration"
description: Delete the computer association between two system resources used in state migration.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# DeleteAssociation Method in Class SMS_StateMigration

The `DeleteAssociation` Windows Management Instrumentation (WMI) class method, in Configuration Manager, deletes the computer association between two system resources used in state migration.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 DeleteAssociation(
      UInt32 SourceClientResourceID,
      UInt32 RestoreClientResourceID
);
```

#### Parameters

`SourceClientResourceID` Data type: `UInt32`

Qualifiers: [in]

Resource ID for the source client.

`RestoreClientResourceID` Data type: `uint32`

Qualifiers: [in]

Resource ID for the destination client.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Remarks

Your application uses this method to remove an association that has been created by using a call to the [AddAssociation Method in Class SMS_StateMigration](addassociation-method-in-class-sms_statemigration.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_StateMigration Server WMI Class](sms_statemigration-server-wmi-class.md) [AddAssociation Method in Class SMS_StateMigration](addassociation-method-in-class-sms_statemigration.md)
