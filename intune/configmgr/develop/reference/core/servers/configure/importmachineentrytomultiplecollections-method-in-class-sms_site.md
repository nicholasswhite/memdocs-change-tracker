---
title: "ImportMachineEntryToMultipleCollections method in class SMS_Site"
description: ImportMachineEntryToMultipleCollections method
ms.date: "2019-04-03T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/68e4b2d8-b70c-4019-b49a-d1f8881e2aea
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/67b2ba1a-6f74-4044-a48a-f0f8ad076b8f
---

# ImportMachineEntryToMultipleCollections method in class SMS_Site

The `ImportMachineEntryToMultipleCollections` WMI class method in Configuration Manager imports computer information and one or more optional collections.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 ImportMachineEntryToMultipleCollections
{
    [IN]    String NetbiosName
    [IN]    String SMBIOSGUID
    [IN]    String MACAddress
    [IN]    Boolean OverwriteExistingRecord
    [IN]    String FQDN
    [IN]    String AdminPassword
    [IN]    Boolean AddToCollection
    [IN]    SMS_CollectionRule CollectionRule
    [IN]    String[] CollectionIds
    [IN]    String WTGUniqueKey
    [OUT]   Boolean MachineExists
    [OUT]   UInt32 ResourceID
    [OUT]   String SMSUniqueIdentifier
};
```

### Parameters

#### `NetbiosName`

Data type: `String`

Qualifiers: [id("0"), in]

The NetBIOS name for the computer.

#### `SMBIOSGUID`

Data type: `String`

Qualifiers: [id("1"), in]

The GUID for the system management BIOS (SMBIOS).

#### `MACAddress`

Data type: `String`

Qualifiers: [id("2"), in]

The MAC address must be for a network adapter that has a driver in Windows PE. The MAC address must be in colon format. For example, 00:00:00:00:00:00. Other formats prevent the client from receiving policy.

#### `OverwriteExistingRecord`

Data type: `Boolean`

Qualifiers: [id("3"), in]

`true` to overwrite the existing record.

#### `FQDN`

Data type: `String`

Qualifiers: [id("4"), in, optional]

Fully qualified domain name of this computer.

#### `AdminPassword`

Data type: `String`

Qualifiers: [id("7"), in, optional]

The changed password of the MEBx password that can occur during out of band provisioning.

#### `AddToCollection`

Data type: `Boolean`

Qualifiers: [id("8"), in, optional]

`true` to add the computer to a collection.

#### `CollectionRule`

Data type: `SMS_CollectionRule`

Qualifiers: [id("9"), in, optional]

Adds the collection rule to a specified collection. The default value is NULL.

#### `CollectionIds`

Data type: `String[]`

Qualifiers: [id("10"), in, optional]

The collection identifier(s) for the collection(s) that the computer is added to. The default value is empty.

#### `WTGUniqueKey`

Data type: `String`

Qualifiers: [id("11"), in, optional]

For a Windows To Go deployment, this is the USB unique key that is used to identify the client, instead of the SMBIOS and MAC address.

#### `MachineExists`

Data type: `Boolean`

Qualifiers: [id("12"), out]

`true` if the computer exists.

#### `ResourceID`

Data type: `UInt32`

Qualifiers: [id("13"), out]

Resource identifier for the computer.

#### `SMSUniqueIdentifier`

Data type: `String`

Qualifiers: [id("14"), out]

Unique identifier of Configuration Manager.

## Runtime requirements

For more information, see [Configuration Manager server runtime requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development requirements

For more information, see [Configuration Manager server development requirements](../../../../core/reqs/server-development-requirements.md).
