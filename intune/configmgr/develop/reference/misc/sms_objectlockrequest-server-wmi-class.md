---
title: "SMS_ObjectLockRequest Server WMI Class"
description: An SMS Provider server class, in Configuration Manager, that represents object lock request information.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_ObjectLockRequest Server WMI Class

The `SMS_ObjectLockRequest` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents object lock request information.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ObjectLockRequest :
{
    String AssignedMachine;
    String AssignedObjectLockContext;
    String AssignedSiteCode;
    DateTime AssignedTimeUTC;
    String AssignedUser;
    UInt32 LockState;
    String ObjectRelPath;
    String RequestID;
    UInt32 RequestState;
};
```

## Methods

The `SMS_ObjectLockRequest` class does not define any methods.

## Properties

`AssignedMachine` Data type: `String`

Access type: Read/Write

Qualifiers: none

Indicates the currently assigned computer of the requested lock.

`AssignedObjectLockContext` Data type: `String`

Access type: Read/Write

Qualifiers: none

Indicates ObjectLockContext the lock is currently assigned to.

`AssignedSiteCode` Data type: `String`

Access type: Read/Write

Qualifiers: none

Indicates the current site of the requested lock.

`AssignedTimeUTC` Data type: `DateTime`

Access type: Read/Write

Qualifiers: none

Indicates the time at which the requested lock was assigned.

`AssignedUser` Data type: `String`

Access type: Read/Write

Qualifiers: none

Indicates the currently assigned user of the requested lock.

`LockState` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Indicates the current state of the requested lock. Possible values are:

| Value | Lock state |
| --- | --- |
| 0 | Unassigned |
| 1 | Assigned |
| 2 | Requested |
| 3 | PendingAssignment |
| 4 | TimedOut |
| 5 | NotFound |

`ObjectRelPath` Data type: `String`

Access type: Read/Write

Qualifiers: none

The path of the object for which the lock is requested.

`RequestID` Data type: `String`

Access type: Read/Write

Qualifiers: none

Unique identifier of the request.

`RequestState` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Request state values. The request states `Granted`, `GrantedAfterTimeout` and `GrantedLockWasOrphaned` indicate a successful request and the user can then make and save modifications to the object. All other requests indicate an error.

| RequestStateID | RequestStateName |
| --- | --- |
| 0 | Unknown |
| 2 | Requested |
| 3 | RequestedCanceled |
| 4 | ResponseReceived |
| 10 | Granted |
| 11 | GrantedAfterTimeout |
| 12 | GrantedLockWasOrphaned |
| 20 | DeniedLockAlreadyAssigned |
| 21 | DeniedInvalidObjectVersion |
| 22 | DeniedLockNotFound |
| 23 | DeniedLockNotLocal |
| 24 | DeniedRequestTimedOut |
| 50 | Error |
| 52 | ErrorRequestNotFound |
| 53 | ErrorRequestTimedOut |

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
