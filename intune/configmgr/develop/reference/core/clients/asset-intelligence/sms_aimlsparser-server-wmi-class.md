---
title: "SMS_AIMLSParser Server WMI Class"
description: In Configuration Manager, the SMS_AIMLSParser Windows Management Instrumentation class imports license data.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/07bb3e10-d135-43ff-bc8b-360497cb39fa
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/12e559b9-eaf6-4aee-9af7-62334e15f863
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
---

# SMS_AIMLSParser Server WMI Class

The `SMS_AIMLSParser` Windows Management Instrumentation (WMI) class in Configuration Manager imports license data.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_AIMLSParser : SMS_BaseClass ();
```

## Methods

The following table lists the methods in the `SMS_AIMLSParser` class.

| Method | Description |
| --- | --- |
| [GetStatus Method in Class SMS_AIMLSParser](getstatus-method-in-class-sms_aimlsparser.md) | Monitors the status of a previous call to the `Import` method. The returned values of the `Status` parameter are:   0 - Successful completion |
| [GetSummary Method in Class SMS_AIMLSParser](getsummary-method-in-class-sms_aimlsparser.md) | Retrieves the counts of imported Microsoft license count and non-Microsoft license count. |
| [Import Method in Class SMS_AIMLSParser](import-method-in-class-sms_aimlsparser.md) | Imports the MLS statement as specified by the `MLSFilepath` parameter (in UNC format) into the Configuration Manager database. |

## Properties

The `SMS_AIMLSParser` class does not define any properties.

## Remarks

Class qualifiers for this class include:

- DisplayName("AI Hinv Classes List")
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
