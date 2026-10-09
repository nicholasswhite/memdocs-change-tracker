---
description: Learn how to define user information of an application in Configuration Manager with SMS_Windows8ApplicationUserInfo.
title: "SMS_Windows8ApplicationUserInfo Client WMI Class"
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

# SMS_Windows8ApplicationUserInfo Client WMI Class

In Configuration Manager, the `SMS_Windows8ApplicationUserInfo` class is a client Windows Management Instrumentation (WMI) class that defines user information of an application.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_Windows8ApplicationUserInfo
{
      String FullName;
      String InstallState;
      String UserAccountName;
      String UserSecurityId;
};
```

## Methods

The `SMS_Windows8ApplicationUserInfo` class does not define any methods.

## Properties

`FullName` Data type: `String`

Access type: Read-only

Qualifiers: [key, read]

Full name of the user.

`InstallState` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Installation state of the package. Possible values are:

| Value | Description |
| --- | --- |
| NotInstalled | The package has not been installed. |
| Staged | The package has been downloaded. |
| Installed | The package is ready for use. |

`UserAccountName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

User account name.

`UserSecurityId` Data type: `String`

Access type: Read-only

Qualifiers: [key, read]

User security identifier.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Inventory Agent Client WMI Classes](inventory-agent-client-wmi-classes.md)
