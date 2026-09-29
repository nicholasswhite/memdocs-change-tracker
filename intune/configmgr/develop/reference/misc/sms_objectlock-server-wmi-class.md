---
title: "SMS_ObjectLock Server WMI Class"
description: The SMS_ObjectLock abstract WMI class represents methods for locking and unlocking global objects.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_ObjectLock Server WMI Class

The `SMS_ObjectLock` abstract Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents methods for locking and unlocking global objects.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ObjectLock : SMS_BaseClass
{
};
```

## Methods

The following table shows the methods in `SMS_ObjectLock`.

| Method | Description |
| --- | --- |
| [CancelLockRequest Method in Class SMS_ObjectLock](cancellockrequest-method-in-class-sms_objectlock.md) | Cancels a lock request. |
| [CancelLockRequests Method in Class SMS_ObjectLock](cancellockrequests-method-in-class-sms_objectlock.md) | Cancels multiple lock requests. |
| [CheckLockRequest Method in Class SMS_ObjectLock](checklockrequest-method-in-class-sms_objectlock.md) | Checks a lock request. |
| [CheckLockRequests Method in Class SMS_ObjectLock](checklockrequests-method-in-class-sms_objectlock.md) | Checks multiple lock requests. |
| [GetLockInformation Method in Class SMS_ObjectLock](getlockinformation-method-in-class-sms_objectlock.md) | Gets current lock information. |
| [ReleaseAllLocks Method in Class SMS_ObjectLock](releasealllocks-method-in-class-sms_objectlock.md) | Releases all locks for a session. |
| [ReleaseLock Method in Class SMS_ObjectLock](releaselock-method-in-class-sms_objectlock.md) | Releases a lock to global object. |
| [ReleaseLocks Method in Class SMS_ObjectLock](releaselocks-method-in-class-sms_objectlock.md) | Releases locks to multiple global objects. |
| [RequestLock Method in Class SMS_ObjectLock](requestlock-method-in-class-sms_objectlock.md) | Synchronously acquires a lock to edit global object. |
| [RequestLockAsync Method in Class SMS_ObjectLock](requestlockasync-method-in-class-sms_objectlock.md) | Asynchronously acquires a lock to edit global objects. |
| [RequestLocks Method in Class SMS_ObjectLock](requestlocks-method-in-class-sms_objectlock.md) | Synchronously acquires a lock to edit a global object. |
| [RequestLocksAsync Method in Class SMS_ObjectLock](requestlocksasync-method-in-class-sms_objectlock.md) | Asynchronously acquires locks to edit multiple global objects. |

## Properties

None.

## Remarks

Class qualifiers for this class include:

- Abstract

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
