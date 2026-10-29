---
title: "SMS_TopThreatsDetected Server WMI Class"
description: The SMS_TopThreatsDetected class summarizes the top threats found in the last 24 hours per collection.
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

# SMS_TopThreatsDetected Server WMI Class

The `SMS_TopThreatsDetected` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that summarizes the top threats found in the last 24 hours per collection.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TopThreatsDetected : SMS_BaseClass
{
    String CollectionID;
    UInt32 MemberCount;
    UInt32 Rank;
    UInt32 ThreatCategoryID;
    UInt64 ThreatID;
    String ThreatName;
    UInt32 TotalMemberCount;
};
```

## Methods

The `SMS_TopThreatsDetected` class does not define any methods.

## Properties

`CollectionID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Identifier of the collection summarized.

`MemberCount` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Count of members with a threat.

`Rank` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Rank of threat exposure in collection (1 is greatest).

`ThreatCategoryID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Category identifier of threat. Possible values are:

| CategoryID | Category |
| --- | --- |
| 1 | Adware |
| 2 | Spyware |
| 3 | Password Stealer |
| 4 | Trojan Downloader |
| 5 | Worm |
| 6 | Backdoor |
| 8 | Trojan |
| 9 | Email Flooder |
| 11 | Dialer |
| 12 | Monitoring Software |
| 13 | Browser Modifier |
| 19 | Joke Program |
| 21 | Software Bundler |
| 22 | Trojan Notifier |
| 23 | Settings Modifier |
| 27 | Potentially Unwanted Software |
| 30 | Exploit |
| 32 | Malware Creation Tool |
| 33 | Remote Control Software |
| 34 | Tool |
| 36 | Trojan Denial of Service |
| 37 | Trojan Dropper |
| 38 | Trojan Mass Mailer |
| 39 | Trojan Monitoring Software |
| 40 | Trojan Proxy Server |
| 42 | Virus |
| 43 | Permitted |
| 44 | Not Yet Classified |
| 46 | Suspicious Behavior |

`ThreatID` Data type: `UInt64`

Access type: Read/Write

Qualifiers: [key]

Threat identifier.

`ThreatName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Name of the threat.

`TotalMemberCount` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Total count of members in the collection.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
