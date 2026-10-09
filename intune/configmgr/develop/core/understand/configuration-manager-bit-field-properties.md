---
title: "Configuration Manager Bit Field Properties"
description: Some Configuration Manager object properties are implemented as bit fields, where individual binary bits of an integer (usually a uint32 data type) are used as Boolean flags to store information
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: article
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/c6f99e62-1cf6-4b71-af9b-649b05f80cce
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3f56b378-07a9-4fa1-afe8-9889fdc77628
---

# Configuration Manager Bit Field Properties

Some Configuration Manager object properties are implemented as bit fields, where individual binary bits of an integer (usually a `uint32` data type) are used as `Boolean` flags to store information. These properties can be difficult to interpret at the user interface because the bit field is often displayed as a decimal number.

For example, the Security User Class Permissions object (`SMS_UserClassPermissions`) contains an integer property called `ClassPermissions`, which is defined as an `int32` data type with the following bit flags:

| Bit | Value |
| --- | --- |
| 0 | READ |
| 1 | MODIFY |
| 2 | DELETE |
| 3 | DISTRIBUTE |
| 4 | CREATE_CHILD |
| 5 | REMOTE_CONTROL |
| 6 | ADVERTISE |
| 7 | MODIFY_RESOURCE |
| 8 | ADMINISTER |
| 9 | DELETE_RESOURCE |
| 10 | CREATE |
| 11 | VIEW_COLL_FILE |
| 12 | READ_RESOURCE |
| 13 | DELEGATE |
| 14 | METER |
| 15 | MANAGESQLCOMMAND |
| 16 | MANAGESTATUSFILTER |

A typical value of this bit field might be 10100000111. Bit 0 is the least significant bit (on the right) and the other bits are counted right to left. Therefore, in this example, the available class permissions include READ, MODIFY, DELETE, ADMINISTER, and CREATE, corresponding to bit fields 0, 1, 2, 8, and 10, respectively.

The difficulty arises when the binary number 10100000111 appears as the decimal number 1287 in a Configuration Manager console display and in how you interpret the bits. The solution is to open the Windows Calculator application (Calc.exe, in the Accessories group). Use the Scientific view, set the calculator for decimal mode, and enter 1287. Use the radio buttons of the calculator to convert to a binary display. The binary bit field 10100000111 appears. You can read the selected bit flags from this display.

> [!NOTE]
>
> In a typical bit field property, many of the bits are unused and have no defined meaning.

## See Also

[Configuration Manager Association Classes](association-classes.md) [Configuration Manager Date and Time Formats](date-and-time-formats.md) [Configuration Manager Embedded Objects](embedded-objects.md) [Configuration Manager Extended WMI Query Language](extended-wmi-query-language.md) [Objects overview](configuration-manager-objects-overview.md) [Configuration Manager Lazy Properties](configuration-manager-lazy-properties.md) [About errors](about-configuration-manager-errors.md) [Configuration Manager Object Security](configuration-manager-object-security.md) [Configuration Manager Special Queries](special-queries.md)
