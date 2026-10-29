---
description: Learn how to connect to the Configuration Manager client Windows Management Instrumentation (WMI) provider, you create a ManagementScope object in the \\\Client\root\ccm namespace.
title: "How to Connect to the Configuration Manager Client WMI Namespace by Using System.Management"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
ms.collection: tier3


ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# How to Connect to the Configuration Manager Client WMI Namespace by Using System.Management

To connect to the Configuration Manager client Windows Management Instrumentation (WMI) provider, you create a `ManagementScope` object in the \\Client\root\ccm namespace.

You use the `ManagementScope` object to read and query WMI objects. For example, [How to Read a WMI Object Using System.Management](how-to-read-a-wmi-object-by-using-system.management.md).

### To connect to the Configuration Manager client WMI provider

1. In Visual Studio, create a new Visual C# Console Project.
2. Add a reference to the System.Management assembly.
3. In the C# source code, add a reference to the System.Management namespace with the following code.
4. `using System.Management;`
5. Create a new class and add the following connection example code.

## Example

The following C# code example creates and returns a `ManagementScope` object on the root\ccm namespace.

For information about calling the sample code, see [How to Call a WMI Class Method by Using System.Management](how-to-call-a-wmi-class-method-by-using-system.management.md).

```c#

public ManagementScope Connect()  
{  
    try  
    {  
        return new ManagementScope(@"root\ccm");  
    }  
    catch (System.Management.ManagementException e)  
    {  
        Console.WriteLine("Failed to connect", e.Message);  
        throw;  
    }  
}  

```

## Compiling the Code

### Namespaces

System

System.Management

### Assembly

System.Management.dll

## Robust Programming

The exception that can be raised is [System.Management.ManagementException](https://learn.microsoft.com/en-us/dotnet/api/system.management.managementexception).

## See Also

[About Configuration Manager WMI Programming](about-configuration-manager-wmi-programming.md)  
 [How to Call a WMI Class Method by Using System.Management](how-to-call-a-wmi-class-method-by-using-system.management.md)  
 [How to Perform an Asynchronous Query by Using System.Management](how-to-perform-an-asynchronous-query-by-using-system.management.md)  
 [How to Perform a Synchronous Query by Using System.Management](how-to-perform-a-synchronous-query-by-using-system.management.md)  
 [How to Read a WMI Object by Using System.Management](how-to-read-a-wmi-object-by-using-system.management.md)
