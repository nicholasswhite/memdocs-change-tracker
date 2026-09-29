---
title: "GetEncryptDecryptKey Method in Class SMS_StateMigration"
description: The GetEncryptDecryptKey WMI class method retrieves the symmetric key that is used to encrypt and decrypt the user state during state migration.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# GetEncryptDecryptKey Method in Class SMS_StateMigration

The `GetEncryptDecryptKey` Windows Management Instrumentation (WMI) class method, in Configuration Manager, retrieves the symmetric key that is used to encrypt and decrypt the user state during state migration.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 GetEncryptDecryptKey(
   String Key
);
```

#### Parameters

`Key` Data type: `String`

Qualifiers: [out]

The encryption key required to restore user state.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_StateMigration Server WMI Class](sms_statemigration-server-wmi-class.md) [AddAssociation Method in Class SMS_StateMigration](addassociation-method-in-class-sms_statemigration.md)
