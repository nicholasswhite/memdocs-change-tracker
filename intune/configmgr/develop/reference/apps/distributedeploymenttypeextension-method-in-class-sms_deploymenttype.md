---
title: "DistributeDeploymentTypeExtension Method in Class SMS_DeploymentType"
description: The DistributeDeploymentTypeExtension Windows Management Instrumentation (WMI) class method, in Configuration Manager, schedules a Deployment Type Extension to be distributed throughout the hierarchy.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# DistributeDeploymentTypeExtension Method in Class SMS_DeploymentType

The `DistributeDeploymentTypeExtension` Windows Management Instrumentation (WMI) class method, in Configuration Manager, schedules a Deployment Type Extension to be distributed throughout the hierarchy.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 DistributeDeploymentTypeExtension (
     string TechnologyExtensionFileName
);
```

#### Parameters

`TechnologyExtensionFileName` Data type: `String`

Qualifiers: [in]

Filename of the technology extension.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_DeploymentType Server WMI Class](sms_deploymenttype-server-wmi-class.md)
