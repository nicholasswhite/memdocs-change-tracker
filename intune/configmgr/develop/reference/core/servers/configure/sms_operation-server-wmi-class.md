---
description: Learn how to use SMS_Operation class in Configuration Manager, which SMS_RbacSecuredObject embeds. This class describes the various operations.
title: "SMS_Operation Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_Operation Server WMI Class

The `SMS_Operation` Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager that is embedded by `SMS_RbacSecuredObject` and describes the various operations.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_Operation :
{
    UInt32 BitFlag;
    Boolean IsTypeWideOperation;
    UInt32 ObjectTypeID;
    String OperationName;
};
```

## Methods

The `SMS_Operation` class doesn't define any methods.

## Properties

`BitFlag` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

The bit flag of the operation. Possible values are:

| N | 2^N | Operation |
| --- | --- | --- |
| 0 | 1 | Read |
| 1 | 2 | Modify |
| 2 | 4 | Delete |
| 3 | 8 | Copy to Distribution Point |
| 4 | 16 | Set Security Scope |
| 5 | 32 | Remote Control |
| 6 | 64 | Not Used |
| 7 | 128 | Modify Resource |
| 8 | 256 | Not Used |
| 9 | 512 | Delete Resource |
| 10 | 1024 | Create   Admin.Add |
| 11 | 2048 | View Collected File   Application.Approve |
| 12 | 4096 | Read Resource |
| 13 | 8192 | Manage Folder Item |
| 14 | 16384 | Meter Site   Collection.Deploy Packages |
| 15 | 32768 | Not Used |
| 16 | 65536 | Manage Status Filters   Collection.Deploy Client Settings |
| 17 | 131072 | Manage Folder |
| 18 | 262144 | ConfigurationItem.Network Access   Site.Modify CH Settings   Collection.EnforceSecurity   SMS_AntimalwareSettings.ReadDefault |
| 19 | 524288 | Site.Import Machine   Collection.Deploy Antimalware Settings |
| 20 | 1048576 | SequencePackage.Create   Task Sequence Media   SMS_DistributionPointGroup.Associate   SMS_BoundaryGroup.AssociateSiteSystem   SMS_SettingsDefinition.ModifyPolicy   Collection.Deploy Applications |
| 21 | 2097152 | Collection.Modify Collection Settings   Site.ModifyConnectorPolicy   SMS_AntimalwareSettings.ModifyDefault |
| 22 | 4194304 | Site.Manage OSD Certificate   MigrationJob.Manage   MigrationSiteMapping.SpecifySourceHierarchy   Collection.Deploy Configuration Items |
| 23 | 8388608 | StateMigration.Recover User State   Collection.Deploy Task Sequences |
| 24 | 16777216 | Collection.Manage BMC |
| 25 | 33554432 | Collection.View BMC |
| 26 | 67108864 | AISoftwareList.Manage AI   Collection.Deploy Software Updates |
| 27 | 134217728 | AISoftwareList.View AI   Collection.Deploy Firewall Policies |
| 28 | 268435456 | RunReport |
| 29 | 536870912 | ModifyReport |

`IsTypeWideOperation` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

`true`, if the operation is type wide.

If the operation is type wide, the user has the permission against all objects of this type, if the user has this operation against any RBA security category. If the operation isn't type wide, then user has the permission against the objects that are assigned to the related RBA security category.

`ObjectTypeID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Type ID of the object.

`OperationName` Data type: `String`

Access type: Read/Write

Qualifiers: [sizelimit("256")]

Name of the operation.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
