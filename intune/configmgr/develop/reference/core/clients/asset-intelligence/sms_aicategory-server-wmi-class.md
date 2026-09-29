---
title: "SMS_AICategory Server WMI Class"
description: In Configuration Manager, the SMS_AICategory Windows Management Instrumentation class categorizes the software entries in the SMS_AISoftwareList Server WMI class.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_AICategory Server WMI Class

The `SMS_AICategory` Windows Management Instrumentation (WMI) class, in Configuration Manager, categorizes the software entries in the `SMS_AISoftwareList` Server WMI class.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_AICategory : SMS_BaseClass
{
      uint32 CategoryID;
      string CategoryName;
      string Description;
      boolean IsLocal;
      uint32 LanguageID;
      uint32 State;
      uint32 Type;
};
```

## Methods

The following table lists the methods in the `SMS_AICategory` class.

| Method | Description |
| --- | --- |
| [GetSummary Method in Class SMS_AICategory](getsummary-method-in-class-sms_aicategory.md) | Returns a summary of all defined categories. |

## Properties

`CategoryID` Data type: `UInt32`

Access type: Read Only

Qualifiers: key

Unique value for the record.

`CategoryName` Data type: `String`

Access type: Read/Write

Qualifiers: None

Category display name.

`Description` Data type: `String`

Access type: Read/Write

Qualifiers: None

Supplemental information that describes what this category is used for.

`IsLocal` Data type: `Boolean`

Access type: Read Only

Qualifiers: None

`true` if this category instance was created locally. Categories that are created locally can be changed. When `false`, the `CategoryName` and `Description` properties are not editable.

`LanguageID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Language the category is written in.

`State` Data type: `UInt32`

Access type: Read Only

Qualifiers: enumeration("STATE_VALIDATED(0), STATE_USER_DEFINED(1)")

Source of the category.

| Value | Description |
| --- | --- |
| 0 | Validated: Created by Microsoft. |
| 1 | User Defined: Created by a user. |

`Type` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Describes the way this category record is used.

| Value | Description |
| --- | --- |
| 0 | Category: Category this software fits into. Example: Antivirus. |
| 1 | Family: Family this software belongs in. Example: Microsoft Office. |
| 2 | Tag: User defined tags which are assigned to the software entries. Example: Installed on a receptionist's computer. |

## Remarks

Class qualifiers for this class include:

- DisplayName("AI Category Table")
- Dynamic
- Provider("ExtnProv")
- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[Initiate Asset Intelligence synchronization](../../../../core/clients/asset-intelligence/how-to-initiate-a-synchronization.md)
