---
title: "SMS_MAMStoreApplication Server WMI Class"
description: The SMS_MAMStoreApplication WMI class is an SMS Provider server class that represents mobile application management store application lists.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
---

# SMS_MAMStoreApplication Server WMI Class

The `SMS_MAMStoreApplication` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents mobile application management (MAM) store application lists.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_MAMStoreApplication : SMS_BaseClass
{
     String IdentityIdentifier;
     Boolean IsManagedBrowser;
     String MAMSDKVersion;
     Boolean PinToProfile;
     UInt32 StoreIdentifier;
     String StoreApplicationIdentifier;
};

```

## Methods

The `SMS_MAMStoreApplication` class does not define any methods.

## Properties

`IdentityIdentifier` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

Identity identifier.

`IsManagedBrowser` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read]

True if managed browser MAM application.

`MAMSDKVersion` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

Version of the MAM SDK.

`PinToProfile` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read]

True if this application pin to profile.

`StoreIdentifier` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

Store identifier.

`StoreApplicationIdentifier` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

Store application identifier.

## Remarks

Class qualifiers for this class include:

- Dynamic
- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
