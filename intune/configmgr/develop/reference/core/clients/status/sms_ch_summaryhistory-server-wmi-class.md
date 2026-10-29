---
description: Learn how to use the SMS_CH_SummaryHistory class to represent client summary histories.
title: "SMS_CH_SummaryHistory Server WMI Class"
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

# SMS_CH_SummaryHistory Server WMI Class

The `SMS_CH_SummaryHistory` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the client summary history.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CH_SummaryHistory : SMS_BaseClass
{
    UInt32 ClientsActive;
    UInt32 ClientsActiveHealthyOrActiveNoResults;
    UInt32 ClientsHealthy;
    UInt32 ClientsInactive;
    UInt32 ClientsRemediationSuccess;
    UInt32 ClientsRemediationTotal;
    UInt32 ClientsTotal;
    UInt32 ClientsUnhealthy;
    String CollectionID;
    DateTime Date;
    String SiteCode;
};
```

## Methods

The `SMS_CH_SummaryHistory` class does not define any methods.

## Properties

`ClientsActiveHealthyOrActiveNoResults` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Count of active, healthy clients and active clients with no results.

`ClientsActive` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Count of active clients.

`ClientsHealthy` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Count of healthy clients.

`ClientsInactive` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Count of inactive clients.

`ClientsRemediationSuccess` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Count of successfully remediated clients.

`ClientsRemediationTotal` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Total count of remediated clients (successful and unsuccessful).

`ClientsTotal` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Total count of clients.

`ClientsUnhealthy` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Count of unhealthy clients.

`CollectionID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Unique auto-generated ID containing eight characters that identifies the collection.

`Date` Data type: `DateTime`

Access type: Read/Write

Qualifiers: [key]

The summary date.

`SiteCode` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Three-letter site code of the site.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
