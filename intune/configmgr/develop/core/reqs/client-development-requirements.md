---
title: "Configuration Manager Client Development Requirements"
description: The Configuration Manager client can be programmed by using programming languages that follow.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/43093068-2dda-408b-b3fe-dfd705c84f78
- https://authoring-docs-microsoft.poolparty.biz/devrel/7696cda6-0510-47f6-8302-71bb5d2e28cf
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/c6f99e62-1cf6-4b71-af9b-649b05f80cce
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/69c76c32-967e-4c65-b89a-74cc527db725
- https://authoring-docs-microsoft.poolparty.biz/devrel/e453d60d-ba7e-43bc-8028-ec38e6b62512
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3f56b378-07a9-4fa1-afe8-9889fdc77628
---

# Configuration Manager Client Development Requirements

The Configuration Manager client can be programmed by using the following programming languages.

## Managed Code

If you are programming the Configuration Manager client by using managed code, you use the System.Management namespace and, where applicable, you use COM Interoperability to access the Configuration Manager automation objects.

### NET Framework

You should have version 4.0 of the Microsoft .NET Framework installed on the development computer and on the computers you want to deploy your .NET Framework application to. To download the .NET Framework redistributable package, see [Download .NET Framework](https://dotnet.microsoft.com/download/dotnet-framework). It is also installed as part of Visual Studio.

## VBScript

You can use VBScript to access the Configuration Manager client WMI namespaces. The client also has a number of COM automation objects that you can use.

For more information about scripting with WMI, see [Windows Management Instrumentation](https://learn.microsoft.com/en-us/windows/win32/wmisdk/wmi-start-page).

## C++

C++ examples are provided for some Configuration Manager technologies where C++ is the most appropriate development language. In most cases, C++ developers should use the VBScript samples as a guide. For more information about using WMI with C++, see [Creating a WMI Application Using C++](https://learn.microsoft.com/en-us/windows/win32/wmisdk/creating-a-wmi-application-using-c-).

## Other Languages

For languages that are not based on .NET Framework, use the VBScript samples as a starting point for accessing Configuration Manager through WMI.

> [!IMPORTANT]
>
> For more information about general Configuration Manager requirements, see [Supported configurations](../../../core/plan-design/configs/supported-configurations.md).

## See Also

[Configuration Manager Server Development Requirements](server-development-requirements.md) [Configuration Manager SDK Libraries and Header Files](configuration-manager-sdk-libraries-and-header-files.md)
