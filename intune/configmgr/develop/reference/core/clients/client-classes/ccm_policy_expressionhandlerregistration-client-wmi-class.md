---
description: Learn how to describe a registered expression handler for a policy with CCM_Policy_ExpressionHandlerRegistration.
title: "CCM_Policy_ExpressionHandlerRegistration Client WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/8b896464-3b7d-4e1f-84b0-9bb45aeb5f64
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/b1d2d671-9549-46e8-918c-24349120dbf5
---

# CCM_Policy_ExpressionHandlerRegistration Client WMI Class

> [!IMPORTANT]
>
> This class supports the Configuration Manager 2007 infrastructure and is not intended to be used directly from your code.

in Configuration Manager, the `CCM_Policy_ExpressionHandlerRegistration` class is a client Windows Management Instrumentation (WMI) class that describes a registered expression handler for a policy. An expression handler is a COM object that implements the `ICcmPolicyExpressionHandler` interface.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class CCM_Policy_ExpressionHandlerRegistration : CCM_Policy_Config
{
      String Clsid;
      String Name;
};
```

## Methods

The `CCM_Policy_ExpressionHandlerRegistration` class does not define any methods.

## Properties

`Clsid` Data type: `String`

Access type: Read/Write

Qualifiers: [Not_Null:ToInstance]

Class ID of the expression handler COM object, in registry format.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Name of the expression handler. The name is the same as the value of the `ExpressionType` property in [CCM_Policy_Expression Client WMI Class](ccm_policy_expression-client-wmi-class.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Policy Agent Client WMI Classes](policy-agent-client-wmi-classes.md) [CCM_Policy_Expression Client WMI Class](ccm_policy_expression-client-wmi-class.md)
