---
title: "SMS_ClientDataSourcesContentStats Server WMI Class"
description: In Configuration Manager, the SMS_ClientDataSourcesContentStats WMI class is an SMS Provider server class that represents client content data sources per package.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_ClientDataSourcesContentStats Server WMI Class

The `SMS_ClientDataSourcesContentStats` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents client content data sources per package.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ClientDataSourcesContentStats : SMS_BaseClass
{
    UInt64 BytesDownloaded;
    String ContentName;
    UInt32 SourceType;
};

```

## Methods

The `SMS_ClientDataSourcesContentStats` class does not define any methods.

## Properties

`BytesDownloaded` Data type: `UInt64`

Access type: Read

Qualifiers: none

Number of bytes downloaded.

`ContentName` Data type: `String`

Access type: Read

Qualifiers: [key, not_null]

The name of the content.

`SourceType` Data type: `UInt32`

Access type: Read

Qualifiers: [key, not_null]

Source type.

## Remarks

Class qualifiers for this class include:

- Dynamic
- Read (read-only)
- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
