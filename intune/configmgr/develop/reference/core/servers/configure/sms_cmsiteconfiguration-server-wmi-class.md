---
description: Learn how to retrieve the site's monitored configuration status, such as the SQL Server port, SQL Server Service Broker port, and SQL Server Firewall port.
title: "SMS_CMSiteConfiguration Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/cbe4ca68-43ac-4375-aba5-5945a6394c20
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/ced846cc-6a3c-4c8f-9dfb-3de0e90e2742
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_CMSiteConfiguration Server WMI Class

The `SMS_CMSiteConfiguration` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that returns the site's monitored configuration status, such as the SQL Server port, SQL Server Service Broker port, and SQL Server Firewall port.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CMSiteConfiguration : SMS_BaseClass
{
    String Configuration;
    DateTime LastEvaluatingTime;
    UInt32 MessageID;
    String Param1;
    String Param2;
    String Param3;
    String Param4;
    String Param5;
    String Param6;
    UInt32 RoleID;
    String RoleName;
    String SiteCode;
    UInt32 State;
};
```

## Methods

The `SMS_CMSiteConfiguration` class does not define any methods.

## Properties

`Configuration` Data type: `String`

Access type: Read-only

Qualifiers: none

Configuration.

`LastEvaluatingTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: none

Last evaluation time.

`MessageID` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Message identifier.

`Param1` Data type: `String`

Access type: Read-only

Qualifiers: none

Parameter 1.

`Param2` Data type: `String`

Access type: Read-only

Qualifiers: none

Parameter 2.

`Param3` Data type: `String`

Access type: Read-only

Qualifiers: none

Parameter 3.

`Param4` Data type: `String`

Access type: Read-only

Qualifiers: none

Parameter 4.

`Param5` Data type: `String`

Access type: Read-only

Qualifiers: none

Parameter 5.

`Param6` Data type: `String`

Access type: Read-only

Qualifiers: none

Parameter 6.

`RoleID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key]

Role identifier.

`RoleName` Data type: `String`

Access type: Read-only

Qualifiers: none

Role name.

`SiteCode` Data type: `String`

Access type: Read-only

Qualifiers: [key]

Site code.

`State` Data type: `UInt32`

Access type: Read-only

Qualifiers: [enumeration]

State.

| Value | State |
| --- | --- |
| 0 | Valid |
| 1 | Failed without Remediation |
| 2 | Failed with remediaton |
| 99 | Unknown |

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Site Configuration Server WMI Classes](site-configuration-server-wmi-classes.md)
