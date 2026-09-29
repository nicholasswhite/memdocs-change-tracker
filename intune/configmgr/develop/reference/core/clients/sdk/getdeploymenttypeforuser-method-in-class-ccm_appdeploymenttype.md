---
title: "GetDeploymentTypeForUser Method in Class CCM_AppDeploymentType"
description: A class method that retrieves the application deployment type property for a user.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# GetDeploymentTypeForUser Method in Class CCM_AppDeploymentType

The `GetDeploymentTypeForUser` Windows Management Instrumentation (WMI) class method in Configuration Manager that retrieves the application deployment type property for a user.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 GetDeploymentTypeForUser
{
    [IN]    String Id
    [IN]    String Revision
    [IN]    String User
    [OUT]   Object DeploymentType
};
```

## Parameters

`Id` Data type: `String`

Qualifiers: [id("0"), in]

Identifier.

`Revision` Data type: `String`

Qualifiers: [id("1"), in]

Revision.

`User` Data type: `String`

Qualifiers: [id("2"), in]

User.

`DeploymentType` Data type: `CCM_AppDeploymentType`

Qualifiers: [id("3"), out]

Deployment type.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
