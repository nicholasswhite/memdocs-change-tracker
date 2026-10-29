---
title: "CCM_UserLogonEvents Client WMI Class"
description: A client class that represents a user logon event.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# CCM_UserLogonEvents Client WMI Class

The `CCM_UserLogonEvents` Client WMI class is a client class, in Configuration Manager, that represents a user logon event.

The following syntax is simplified from the Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
class CCM_UserLogonEvents
{
    UInt64 LogoffTime;
    UInt64 LogonTime;
    String UserSID;
};

```

## Methods

The `CCM_UserLogonEvents` class does not define any methods.

## Properties

`LogoffTime` Data type: `UInt64`

Access type: Read/Write

Qualifiers: none

The number of seconds elapsed since midnight (00:00:00), January 1, 1970, Coordinated Universal Time (UTC).

`LogonTime` Data type: `UInt64`

Access type: Read/Write

Qualifiers: [key]

The number of seconds elapsed since midnight (00:00:00), January 1, 1970, Coordinated Universal Time (UTC).

`UserSID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

The SID of the user.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).
