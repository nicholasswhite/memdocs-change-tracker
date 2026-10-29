---
title: "SMS_ClientBaselineStatus Server WMI Class"
description: The SMS_ClientBaselineStatus WMI class is an SMS Provider server class, in Configuration Manager, that represents a client deployment baseline status.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_ClientBaselineStatus Server WMI Class

The `SMS_ClientBaselineStatus` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a client deployment baseline status.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ClientBaselineStatus: SMS_BaseClass
{
    UInt32 BaselineType;
    String InstalledClientVersion;
    UInt32 LastErrorCode;
    UInt32 ResourceID;
    String  SMSID;
    UInt32 Status;
};

```

## Methods

The following table lists the methods in the `SMS_ClientBaselineStatus` class.

| Method | Description |
| --- | --- |
| [GetClientBaselineStatusSummary Method in Class SMS_ClientBaselineStatus](getclientbaselinestatussummary-method-in-class-sms_clientbaselinestatus.md) | Gets baseline status summary information by BaselineType and CollectionID. |

## Properties

`BaselineType` Data type: `uint32`

Access type: Read-only

Qualifiers: [read]

The client baseline type. Possible values are:

| Value | Client baseline type |
| --- | --- |
| 1 | Production |
| 2 | Staging |

`InstalledClientVersion` Data type: `String`

Access type: Read/Write

Qualifiers: none

Client version that deployed through client deployment.

`LastErrorCode` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

The last error code sent by the client.

`ResourceID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, read]

Resource ID of the client.

`SMSID` Data type: `String`

Access type: Read-only

Qualifiers: [read]

The SMSID of the client.

`Status` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

The status of the client against the client baseline. Possible values are:

| Value | Client status |
| --- | --- |
| 1 | Compliant |
| 2 | InProgress |
| 3 | NotCompliant |
| 4 | CriticalError |

## Remarks

Class qualifiers for this class include:

- Dynamic

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
